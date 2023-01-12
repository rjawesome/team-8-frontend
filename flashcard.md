## Flashcard

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
 /* The flip card container - set the width and height to whatever you want. We have added the border property to demonstrate that the flip itself goes out of the box on hover (remove perspective if you don't want the 3D effect */
.flip-card {
  background-color: transparent;
  width: 300px;
  height: 200px;
  border: 1px solid #f1f1f1;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flipped {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Style both sides */
.flip-card-front, .flip-card-back {
  background-color: dodgerblue;
  color: white;
}

/* Style the back side */
.flip-card-back {
  transform: rotateY(180deg);
}
</style>
