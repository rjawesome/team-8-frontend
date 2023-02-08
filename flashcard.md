## Flashcard

<link rel="stylesheet" href="{{ '/assets/css/flashcard.css?v=' | append: site.github.build_revision | relative_url }}">
<p id="counter">1/1</p>
<div class="flip-card" id="flipcard">
  <div class="flip-card-inner" id="inner-flipcard" onclick="flipCard()">
    <div class="flip-card-front" id = "front">
      
    </div>
    <div class="flip-card-back" id = "back">

    </div>
  </div>
</div>
<button onclick="backward()">⬅️</button>
<button onclick="forward()">➡️</button>

<button class="answer-btn" style="display: none;" onclick="forward()">❌</button>
<button class="answer-btn" style="display: none;" onclick="forward()">☑️</button>

<script>
  var flipped = false
  const flipCard = () => {
    flipped = !flipped
    document.getElementById("inner-flipcard").classList.toggle("flipped")
    for (b of document.getElementsByClassName("answer-btn")) {
      b.style.display = b.style.display === "none" ? "inline-block" : "none";
    }
  }


  const ID = 20; // will be inputted by user later
  var flashcards = [];
  var currentFlashcard = 0;

  fetch("https://csa-backend.rohanj.dev/api/flashcard/getFlashcardSet",
    { 
      method: 'POST',  
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({id: ID})
    }
  ).then(response => {
    response.json().then(data => {
      console.log(data);
      const flashcardSet = data.flashcards;
      flashcards = flashcardSet;
      document.getElementById("front").innerHTML = flashcardSet[0].front;
      document.getElementById("back").innerHTML = flashcardSet[0].back;
      document.getElementById("counter").innerHTML = "1/" + flashcardSet.length;
      
      flashcardSet.forEach((flashcard, index) => {
        console.log(flashcard);
        console.log(flashcard.front);
        
      })
    })
  })

  function forward() {
    if (currentFlashcard >= flashcards.length-1) {
      return;
    }
    currentFlashcard++;

    setTimeout(() => {
      document.getElementById("front").innerHTML = flashcards[currentFlashcard].front;
      document.getElementById("back").innerHTML = flashcards[currentFlashcard].back;
      document.getElementById("counter").innerHTML = (currentFlashcard+1) + "/" + flashcards.length;
    }, flipped ? 275 : 0)

    if (flipped) {
      flipCard();
    }
  }

  function backward() {
    if (currentFlashcard <= 0) {
      return;
    }
    currentFlashcard--;

    setTimeout(() => {
      document.getElementById("front").innerHTML = flashcards[currentFlashcard].front;
      document.getElementById("back").innerHTML = flashcards[currentFlashcard].back;
      document.getElementById("counter").innerHTML = (currentFlashcard+1) + "/" + flashcards.length;
    }, flipped ? 275 : 0)

    if (flipped) {
      flipCard();
    }
  }

</script>

<style>
</style>
