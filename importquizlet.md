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
	<label for="setName">Set Name:</label>
  <input type="text" id="setName" name = "setName" class="form-control">
  <label>Quizlet Link:
    <input type="text" id="enter-link" name="enter-link" placeholder="Link">
  </label><br>
  <input type="checkbox" id="public-check" name="public-check">Public
  <button type="button" id="submit-set-button">Submit</button>
	
</form>


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

  const flashcardSet = document.getElementById("import-quizlet");
  const setLink = document.getElementById("enter-link");
  const publicCheck = document.getElementById("public-check");
  
  document.getElementById("submit-set-button").onclick = (e) => {
	  e.preventDefault()
    const flashcardSet = { email: "rohanj2006@gmail.com", password: "password", id: setLink.value.split("quizlet.com/").splice(-1)[0].split("/")[0]};

    var url = "https://csa-backend.rohanj.dev/api/flashcard/getQuizlet";
    const options = {
            method: 'POST', // *GET, POST, PUT, DELETE, etc.
            headers: {
            'Content-Type': 'application/json'
            // 'Content-Type': 'application/x-www-form-urlencoded',
            },
            body: JSON.stringify(flashcardSet) // body data type must match "Content-Type" header
        };
        fetch(url, options).then(response => {
            if (response.status >= 400) {
	       alert("Bad Quizlet URL")
	       return;
	    }
            response.json().then(data => {
				const input = data;
				const output = [];

				for (const key in input) {
				  const value = input[key];
				  output.push({front: key, back: value});
				}

				console.log(output);
				const flashcardData = { email: "rohanj2006@gmail.com", password: "password", name: document.getElementById("setName").value, isPublic: publicCheck.checked, flashcards: output};
				const flashcardsJson = JSON.stringify(flashcardData);
				console.log(flashcardsJson);

				var url = "https://csa-backend.rohanj.dev/api/flashcard/createFlashcardSet";
				const options = {
					method: 'POST', // *GET, POST, PUT, DELETE, etc.
					headers: {
					'Content-Type': 'application/json'
					// 'Content-Type': 'application/x-www-form-urlencoded',
					},
                                        credentials: 'include',
					body: flashcardsJson // body data type must match "Content-Type" header
				};
				fetch(url, options).then(response => {

					response.json().then(data => {
					console.log(data);
					window.location = `/flashcard.html?id=` + data.id;
					})
				})

				.catch(err => {
					console.log("Error: " + err);
				})
			})
        })
        .catch(err => {
            console.log("Error: " + err);
        })
  }
</script>
