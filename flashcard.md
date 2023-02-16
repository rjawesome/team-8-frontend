## Flashcard

<link rel="stylesheet" href="{{ '/assets/css/flashcard.css?v=' | append: site.github.build_revision | relative_url }}">
<p id="counter">1/1</p>
<div class="flip-card" id="flipcard" name="flipcard">
  <div class="flip-card-inner" id="inner-flipcard" onclick="flipCard()">
    <div class="flip-card-front" id = "front">
      
    </div>
    <div class="flip-card-back" id = "back">

    </div>
  </div>
</div>
<button onclick="backward()">⬅️</button>
<button onclick="forward()">➡️</button>

<button class="answer-btn" style="display: none;" onclick="sendIncorrect()">❌</button>
<button class="answer-btn" style="display: none;" onclick="sendCorrect()">☑️</button>


<script>
  
  var flipped = false
  const flipCard = () => {
    flipped = !flipped
    document.getElementById("inner-flipcard").classList.toggle("flipped")
    for (b of document.getElementsByClassName("answer-btn")) {
      b.style.display = b.style.display === "none" ? "inline-block" : "none";
    }
  }


  var currentUrl = window.location.href;
  let url = new URL(currentUrl);                                                  
  let urlParams = new URLSearchParams(url.search); 


  const ID = parseInt(urlParams.get('id')); // will be inputted by user later
  if (ID === null || isNaN(ID)) {
    window.location.pathname = "/search.html";
  }
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

      document.getElementsByName("flipcard")[0].id = flashcardSet[0].id;
      
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
      console.log(flashcards[currentFlashcard].id);
      document.getElementsByName("flipcard")[0].id = flashcards[currentFlashcard].id;
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

  function sendIncorrect() {
    sendStats(false);
    forward();
  }

  function sendCorrect() {
    sendStats(true);
    forward();
  }

  function sendStats(isCorrect) {
    fetch("https://csa-backend.rohanj.dev/api/stats/createStats",
      { 
        method: 'POST',  
        headers: {
          'Content-Type': 'application/json'
        },
        credentials: 'include',
        body: JSON.stringify({email: "rohanj2006@gmail.com", password: "password", id: flashcards[currentFlashcard].id, correct: isCorrect})
      }
    ).then(response => {
      response.json().then(data => {
        console.log(data);
      })
    })
  }

</script>

<style>
</style>
