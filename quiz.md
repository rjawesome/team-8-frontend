<link rel="stylesheet" href="{{ '/assets/css/quiz.css?v=' | append: site.github.build_revision | relative_url }}">

<h2>Practice Quiz</h2>
<ul class="quiz" id="quiz">

</ul>
<button class="view-results" onclick="returnScore()" id="check">Check</button>
<span id="myresults" class="my-results">Your score is -/-</span>

<script>
  fetch("https://csa-backend.rohanj.dev/api/login/getYourUser",
    { 
        method: 'POST',  
        headers: {
            'Content-Type': 'application/json'
        },
        body: '{}',
        credentials: 'include'
        }
        ).then(data => {
            if (data.status != 200) {
            window.location.href = "/login"
            data.json().then(console.log)
            } else {
            return data.json()
            }
    })


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
    credentials: 'include',
    body: JSON.stringify({id: ID})
  }
).then(data => data.json())
.then(data => {
  var qNum = 0;
  Object.keys(data).forEach(q => {
    datas.push(data[q]);
    const container = document.createElement("li")
    const qElem = document.createElement("h4")
    qElem.innerHTML = "What definition matches this term: " + q;
    qElem.id = "q"+qNum;
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
      span.innerHTML = ans.ans;
      label.appendChild(input);
      label.appendChild(span);
      li.appendChild(label);
      choices.appendChild(li);
  
      if (ans.ind === 0) correctAnswer = index;
    })
    
    container.appendChild(choices)

    document.getElementById("quiz").appendChild(container)

    answers = [...answers, correctAnswer.toString()]
    qNum++
  })
})

function getCheckedValue(radioName) {
    var radios = document.getElementsByName(radioName);
    var ret = undefined;
    for (var y = 0; y < radios.length; y++) {
        // disable radio
        radios[y].disabled = true
        if (radios[y].checked) ret = radios[y].value;
    }
    return ret;
}
function getScore(email, password) {
    // disable submit button
    document.getElementById("check").disabled = true
    var score = 0;
    var statsInfo = {email, password, id: ID, statsList: []}
    for (var i = 0; i < answers.length; i++) {
       if (getCheckedValue("question" + i) === answers[i]) {
          score++;
          statsInfo.statsList.push({id: datas[i].id, correct: true}) 
       } else {
          document.getElementById("q"+i).style.color = 'red'
          statsInfo.statsList.push({id: datas[i].id, correct: false})
       }
    }
    return {score, statsInfo};
}
function returnScore() {
    var { score, statsInfo } = getScore("rohanj2006@gmail.com", "password")
    document.getElementById("myresults").innerHTML =
        "Your score is " + score + "/" + answers.length;
    console.log(statsInfo)
 
    // send stats
    fetch("https://csa-backend.rohanj.dev/api/stats/createStatsBatch", {
       method: 'POST',
       headers: {
         'Content-Type': 'application/json'
       },
       credentials: 'include',
       body: JSON.stringify(statsInfo)
    });
}
</script>
