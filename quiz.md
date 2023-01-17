<link rel="stylesheet" href="{{ '/assets/css/quiz.css?v=' | append: site.github.build_revision | relative_url }}">

<h2>Practice Quiz</h2>
<ul class="quiz">
  <li>
      <h4>Which term matches this definiton: The first method that runs in a class before any other method. Allows for the initialization and declaration of variables so that way the variables can be used in the project?</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question0" value="A" /><span
                      >Class</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="B" /><span
                      >Control Structure</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="C" /><span
                      >Constructor</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="D" /><span
                      >Abstract Class</span
                  ></label
              >
          </li>
      </ul>
  </li>
  <li>
      <h4>Which term matches the type of iteration that continuously runs until the condition(s) are no longer met?</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question1" value="A" /><span
                      >if</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="B" /><span
                      >while</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="C" /><span
                      >for</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="D" /><span
                      >else</span
                  ></label
              >
          </li>
      </ul>
  </li>
  <li>
      <h4>Match this definition with the primitive data type it is most similar to: used to represent a single true/false value</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question2" value="A" /><span
                      >double</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="B" /><span
                      >int</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="C" /><span
                      >float</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="D" /><span
                      >boolean</span
                  ></label
              >
          </li>
      </ul>
  </li>
</ul>
<button class="view-results" onclick="returnScore()">Check</button>
<span id="myresults" class="my-results">Your score is -/3</span>

<script>
  // Answer sheet
var answers = ["C", "B", "D"],
    tot = answers.length;
function getCheckedValue(radioName) {
    var radios = document.getElementsByName(radioName);
    for (var y = 0; y < radios.length; y++)
        if (radios[y].checked) return radios[y].value;
}
function getScore() {
    var score = 0;
    for (var i = 0; i < tot; i++)
        if (getCheckedValue("question" + i) === answers[i]) score += 1;
    return score;
}
function returnScore() {
    document.getElementById("myresults").innerHTML =
        "Your score is " + getScore() + "/" + tot;
    if (getScore() > 2) {
        console.log("Bravo");
    }
}
</script>
