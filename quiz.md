<link rel="stylesheet" href="{{ '/assets/css/quiz.css?v=' | append: site.github.build_revision | relative_url }}">

<h2>Practice Quiz</h2>
<ul class="quiz" id="quiz">

</ul>
<button class="view-results" onclick="returnScore()">Check</button>
<span id="myresults" class="my-results">Your score is -/3</span>

<script>
 function shuffle(array) {
  let currentIndex = array.length,  randomIndex;

  // While there remain elements to shuffle.
  while (currentIndex != 0) {

    // Pick a remaining element.
    randomIndex = Math.floor(Math.random() * currentIndex);
    currentIndex--;

    // And swap it with the current element.
    [array[currentIndex], array[randomIndex]] = [
      array[randomIndex], array[currentIndex]];
  }

  return array;
}
 
  
  
var currentUrl = window.location.href;
let url = new URL(currentUrl);                                                  
let urlParams = new URLSearchParams(url.search); 


const ID = parseInt(urlParams.get('id')); // will be inputted by user later
if (ID === null || isNaN(ID)) {
  window.location.pathname = "/search.html";
}

var answers = [];
var datas = [];

fetch("https://csa-backend.rohanj.dev/api/flashcard/getFlashcardSetMC",
  { 
    method: 'POST',  
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({id: ID})
  }
).then(data => data.json())
.then(data => {
  var qNum = 0;
  Object.keys(data).forEach(q => {
    datas.push(q);
    const container = document.createElement("li")
    const qElem = document.createElement("h4")
    qElem.innerHTML = "What definition matches this term: " + q;
    container.appendChild(qElem)

    const choices = document.createElement("ul")
    choices.classList = "choices"
  
    var randAnswers = shuffle(data[q].answers.map((e, i) => ({ans: e, ind: i})))
    var correctAnswer = -1;

    randAnswers.forEach((ans, index) => {
      const li = document.createElement("li")
      const label = document.createElement("label")
      const input = document.createElement("input")
      input.type = "radio"
      input.name = "question"+qNum;
      input.value = index.toString();
      const span = document.createElement("span")
      span.innerHTML = ans;
      label.appendChild(input);
      label.appendChild(span);
      li.appendChild(label);
      choices.appendChild(li);
  
      if (ans.ind === 0) correctAnswer = index;
    })
    
    container.appendChild(choices)

    document.getElementById("quiz").appendChild(container)

    answers = [...answers, correctAnswer.toString]
    qNum++
  })
})

function getCheckedValue(radioName) {
    var radios = document.getElementsByName(radioName);
    for (var y = 0; y < radios.length; y++)
        if (radios[y].checked) return radios[y].value;
}
function getScore() {
    var score = 0;
    for (var i = 0; i < answers.length; i++)
        if (getCheckedValue("question" + i) === answers[i]) score += 1;
    return score;
}
function returnScore() {
    document.getElementById("myresults").innerHTML =
        "Your score is " + getScore() + "/" + answers.length;
    if (getScore() > 2) {
        console.log("Bravo");
    }
}
</script>
