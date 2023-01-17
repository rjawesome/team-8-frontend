<link rel="stylesheet" href="{{ '/assets/css/quiz.css?v=' | append: site.github.build_revision | relative_url }}">

<h2>Practice Quiz</h2>
<ul class="quiz">
  <li>
      <h4>Which of the following is not a Java feature?</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question0" value="A" /><span
                      >Dynamic</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="B" /><span
                      >Architecture Neutral</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="C" /><span
                      >Use of pointers</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question0" value="D" /><span
                      >Object-oriented</span
                  ></label
              >
          </li>
      </ul>
  </li>
  <li>
      <h4>How many states are there in America?</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question1" value="A" /><span
                      >48</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="B" /><span
                      >50</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="C" /><span
                      >52</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question1" value="D" /><span
                      >60</span
                  ></label
              >
          </li>
      </ul>
  </li>
  <li>
      <h4>What year did World War II end?</h4>
      <ul class="choices">
          <li>
              <label
                  ><input type="radio" name="question2" value="A" /><span
                      >1896</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="B" /><span
                      >1918</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="C" /><span
                      >1942</span
                  ></label
              >
          </li>
          <li>
              <label
                  ><input type="radio" name="question2" value="D" /><span
                      >1945</span
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
