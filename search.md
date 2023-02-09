<link rel="stylesheet" href="{{ '/assets/css/search.scss?v=' | append: site.github.build_revision | relative_url }}">

<h2>Flashcard Search</h2>
  <body>
    <form id="form">
      <input type="text" id="search-bar" placeholder="Search for flashcard sets">
      <button type="submit">Search</button>
    </form>
    <table id="flashcard-sets-table">
      <thead>
        <tr>
          <th>Flashcard Sets:</th>
          <th>Quiz:</th>
          <th>Flashcards:</th>
        </tr>
      </thead>
      <tbody id="flashcard-sets-container"></tbody>
    </table>
  </body>
  <script>
    // add event listener for form submission
  document.getElementById("form").onsubmit = (function(event) {
  event.preventDefault();
  var searchTerm = document.getElementById("search-bar").value;
  // send searchTerm and classFilter to server or perform search logic here
  document.getElementById("flashcard-sets-container").innerHTML = '';
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
        var flashcardSetRow = document.createElement("tr");
        var flashcardSetElem = document.createElement("td");
        var flashcardSetName = document.createElement("p");
        var mcButtonA = document.createElement("a")
        mcButtonA.href = "/quiz?id=" + data.id;
        mcButtonA.innerHTML = "mc"
        var mcButton = document.createElement("td")
        mcButton.appendChild(mcButtonA)
        var flashButtonA = document.createElement("a")
        flashButtonA.href = "/flashcard?id=" + data.id;
        flashButtonA.innerHTML = "flash"
        var flashButton = document.createElement("td")
        flashButton.appendChild(flashButtonA)
        flashcardSetName.innerHTML = data.name;
        flashcardSetElem.appendChild(flashcardSetName)
        // flashcardSetElem.appendChild(mcButton)
        // flashcardSetElem.appendChild(flashButton)


        flashcardSetRow.appendChild(flashcardSetElem);
        flashcardSetRow.appendChild(mcButton)
        flashcardSetRow.appendChild(flashButton)
        document.getElementById("flashcard-sets-container").appendChild(flashcardSetRow);
      })
    });
  })
    </script>
