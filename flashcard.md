## Flashcard

<link rel="stylesheet" href="{{ '/assets/css/flashcard.css?v=' | append: site.github.build_revision | relative_url }}">

<div class="flip-card" id="flipcard">
  <div class="flip-card-inner" id="inner-flipcard">
    <div class="flip-card-front">
      Front
    </div>
    <div class="flip-card-back">
      Back
    </div>
  </div>
</div>

<script>
  document.getElementById("inner-flipcard").onclick = () => {
    document.getElementById("inner-flipcard").classList.toggle("flipped")
  }
</script>

<style>
</style>
