<link rel="stylesheet" href="{{ '/assets/css/search.scss?v=' | append: site.github.build_revision | relative_url }}">

<h2>Your Flashcard Sets</h2>
  <body>
    <table id="flashcard-sets-table">
      <thead>
        <tr>
          <th>Flashcard Sets:</th>
          <th>Quiz:</th>
          <th>Flashcards:</th>
          <th>Stats:</th>
        </tr>
      </thead>
      <tbody id="flashcard-sets-container"></tbody>
    </table>
  </body>
  <script>
    // add event listener for form submission
  document.getElementById("flashcard-sets-container").innerHTML = '';
  fetch("https://csa-backend.rohanj.dev/api/flashcard/getYourFlashcardSets",
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
        var statsButtonA = document.createElement("a")
        statsButtonA.href = "/stats?id=" + data.id;
        statsButtonA.innerHTML = "stats"
        var statsButton = document.createElement("td")
        statsButton.appendChild(statsButtonA)
        // flashcardSetElem.appendChild(mcButton)
        // flashcardSetElem.appendChild(flashButton)
        flashcardSetRow.appendChild(flashcardSetElem);
        flashcardSetRow.appendChild(mcButton)
        flashcardSetRow.appendChild(flashButton)
        flashcardSetRow.appendChild(statsButton)
        document.getElementById("flashcard-sets-container").appendChild(flashcardSetRow);
      })
    });
    </script>
