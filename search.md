<h2>Flashcard Search</h2>
  <body>
    <form id="form">
      <input type="text" id="search-bar" placeholder="Search for flashcard sets">
      <button type="submit">Search</button>
    </form>
    <div id="flashcard-sets-container"></div>

  </body>
  <script>
    // add event listener for form submission
document.getElementById("form").onsubmit = (function(event) {
  event.preventDefault();
  var searchTerm = document.getElementById("search-bar").value;
  // send searchTerm and classFilter to server or perform search logic here
  fetch("https://csa-backend.rohanj.dev/api/flashcard/getFlashcardSetsByName",
{ 
  method: 'POST',  
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({name: searchTerm})
  }
  ).then(data => data.json())
    .then(data => {
      data.forEach(data => {
        var flashcardSet = document.createElement("div");
        flashcardSet.classList.add("flashcard-set");
        flashcardSet.innerHTML = data.name;
        document.getElementById("flashcard-sets-container").appendChild(flashcardSet);
      })
    });
  })
    </script>