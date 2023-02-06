<link rel="stylesheet" href="{{ '/assets/css/createcard.css?v=' | append: site.github.build_revision | relative_url }}">

<div id="flashcard-container"></div>

<form id="flashcard-form">
  <label for="setName">Set Name:</label>
  <input type="text" id="setName" name = "setName">
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
    const flashcardSet = [];
    const flashcards = [];
    for (let i = 0; i < flashcardCount; i++) {
      const term = document.getElementById(`term-${i}`).value;
      const definition = document.getElementById(`definition-${i}`).value;
      flashcardSet.push({ front: term, back: definition });
    }
    flashcards.push({ email: "rohanj2006@gmail.com", password: "password", name: document.getElementById("setName").value, isPublic: publicCheck.checked, flashcards: flashcardSet});
    const flashcardsJson = JSON.stringify(flashcards);
    console.log(flashcardsJson);
  });
</script>