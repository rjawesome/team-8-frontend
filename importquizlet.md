<h2>Import Quizlets from Online</h2>
<ul class="quizlet" id="quizlet"></ul>

<button class="get-quizlet" onclick="getQuizlet()">Import</button>

<script>
const ID = 20; // will be inputted by user later

fetch("https://csa-backend.rohanj.dev/api/#changethis#",
  { 
    method: 'POST',  
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({id: ID})
  }
).then(data => data.json())
</script>