<h2>Import Quizlets from Online</h2>
<ul class="import" id="import"></ul>

<style>
  .form-control{
    display:block;width:100%;
    padding:.375rem .75rem;
    font-size:1rem;
    font-weight:400;
    line-height:1.5;
    color:black;
    background-color:white;
    background-clip:padding-box;
    border:1px solid white;
    -webkit-appearance:none;
    -moz-appearance:none;
    appearance:none;
    border-radius:.375rem;
    transition:border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  }
</style>

  <label>Quizlet Link:
    <input type="text" id="enter-link" name="enter-link">
  </label><br>
  <input type="checkbox" id="public-check" name="public-check">Public
  <button type="button" id="submit-set-button">Submit</button>


<script>
  async function createFlashcardSet() {
    const response = await fetch("https://csa-backend.rohanj.dev/api/flashcard/createFlashcardSet");
    const data = await response.json();

    let table = "<table><tr><th>Key</th><th>Value</th></tr>";
    for (let key in data) {
      table += "<tr><td>" + key + "</td><td>" + data[key] + "</td></tr>";
    }
    table += "</table>";

    document.getElementById("flashcardSet").innerHTML = table;
  }
</script>
<body onload="createFlashcardSet()">
<div id="flashcardSet"></div>
</body>
