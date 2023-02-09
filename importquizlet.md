<h2>Import Quizlets from Online</h2>
<ul class="quizlet" id="quizlet"></ul>

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

<form id="flashcard-form">
  <label for="setName">Set Name:</label>
  <input type="text" id="setName" name = "setName" class="form-control" placeholder="test">
  <div id="flashcard-inputs-0" class="card-input">
    <table>
      <thead>
        <tr>
          <th><label for="term-0">Term:</label></th>
          <th><label for="definition-0">Definition:</label></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><input type="text" id="term-0" name="term-0"></td>
          <td><input type="text" id="definition-0" name="definition-0"></td>
        </tr>
      </tbody>
    </table>
  </div>
  <button type="button" id="add-card-button">Add Card</button><br>
  <label>Class:
    <input type="text" id="set-class" name="set-class">
  </label><br>
  <input type="checkbox" id="public-check" name="public-check">Public
  <button type="button" id="submit-card-button">Submit</button>
</form>

<script>
  const flashcardContainer = document.getElementById("flashcard-container");
  const flashcardForm = document.getElementById("flashcard-form");
  const addCardButton = document.getElementById("add-card-button");
  const submitButton = document.getElementById("submit-card-button");
  const publicCheck = document.getElementById("public-check");
  const setClass = document.getElementById("set-class");
  let flashcardCount = 1;

  addCardButton.addEventListener("click", function() {
    const flashcardInputs = document.createElement("div");
    flashcardInputs.classList.add("card-input");
    flashcardInputs.id = `flashcard-inputs-${flashcardCount}`;
    flashcardInputs.innerHTML = `
      <table>
      <thead>
        <tr>
          <th><label for="term-${flashcardCount}">Term:</label></th>
          <th><label for="definition-${flashcardCount}">Definition:</label></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><input type="text" id="term-${flashcardCount}" name="term-${flashcardCount}"></td>
          <td><input type="text" id="definition-${flashcardCount}" name="definition-${flashcardCount}"></td>
        </tr>
      </tbody>
    </table>
    `;
    flashcardForm.insertBefore(flashcardInputs, addCardButton);
    flashcardCount++;
  });

  submitButton.addEventListener("click", function() {
    event.preventDefault();
    const flashcards = [];
    for (let i = 0; i < flashcardCount; i++) {
      const term = document.getElementById(`term-${i}`).value;
      const definition = document.getElementById(`definition-${i}`).value;
      flashcards.push({ front: term, back: definition });
    }
    const flashcardSet = { email: "rohanj2006@gmail.com", password: "password", name: document.getElementById("setName").value, isPublic: publicCheck.checked, flashcards};
    const flashcardsJson = JSON.stringify(flashcardSet);
    console.log(flashcardsJson);

    var url = "https://csa-backend.rohanj.dev/api/flashcard/createFlashcardSet";
    const options = {
            method: 'POST', // *GET, POST, PUT, DELETE, etc.
            headers: {
            'Content-Type': 'application/json'
            // 'Content-Type': 'application/x-www-form-urlencoded',
            },
            body: flashcardsJson // body data type must match "Content-Type" header
        };
        fetch(url, options).then(response => {

            response.json().then(data => {
                console.log(data);
                window.location = `/import?id=` + data.id;
            })
        })

        .catch(err => {
            console.log("Error: " + err);
        })
  });
</script>
