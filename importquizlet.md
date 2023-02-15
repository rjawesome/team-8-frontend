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



<form id="import-quizlet">
  <label>Quizlet Link:
    <input type="text" id="enter-link" name="enter-link">
  </label><br>
  <button type="button" id="submit-set-button">Submit</button>
</form>


<script>
  const flashcardForm = document.getElementById("import-quizlet");
  const setLink = document.getElementById("enter-link");

  document.getElementById("submit-set-button").onclick = (e) => {
    e.preventDefault();
    const flashcardSet = { email: "rohanj2006@gmail.com", password: "password", id: setLink.value.split("quizlet.com/").splice(-1)[0].split("/")[0] };

    var url = "https://csa-backend.rohanj.dev/api/flashcard/getQuizlet";
    const options = {
      method: 'POST', // *GET, POST, PUT, DELETE, etc.
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(flashcardSet)
    };
    fetch(url, options).then(response => {
      response.json().then(data => {
        console.log(data);

        // create a new <p> tag and set its content to the extracted id
        const idElement = document.createElement("p");
        idElement.textContent = "Extracted id: " + data.id;

        // append the new element to the DOM
        const importList = document.getElementById("import");
        importList.appendChild(idElement);

        // navigate to the flashcard page with the extracted id
        window.location = `/flashcard.html?id=${data.id}`;
      });
    }).catch(err => {
      console.log("Error: " + err);
    });
  }
</script>




