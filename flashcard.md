## Flashcard

<link rel="stylesheet" href="{{ '/assets/css/flashcard.css?v=' | append: site.github.build_revision | relative_url }}">

<div class="flip-card" id="flipcard">
  <div class="flip-card-inner" id="inner-flipcard" onclick="flipCard()">
    <div class="flip-card-front">
      Constructor
    </div>
    <div class="flip-card-back">
      The first method that runs in a class before any other method. Allows for the initialization and declaration of variables so that way the variables can be used in the project?
    </div>
  </div>
</div>
<button class="answer-btn" style="display: none;" onclick="flipCard()">❌</button>
<button class="answer-btn" style="display: none;" onclick="flipCard()">☑️</button>

<script>
  const flipCard = () => {
    document.getElementById("inner-flipcard").classList.toggle("flipped")
    for (b of document.getElementsByClassName("answer-btn")) {
      b.style.display = b.style.display === "none" ? "inline-block" : "none";
    }
  }
</script>

<style>
</style>
