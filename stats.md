
<html>
  <head>
    <title>FlashcardStats</title>
  </head>
  <body>
    <h2>Flashcard Stats</h2>
    <form id="form">
      <input type="text" id="search-bar" placeholder="Search for flashcard sets">
      <button type="submit">Search</button>
    </form>
    <table id="flashcard-sets-table">
      <thead>
        <tr>
          <th>Flashcard Set:</th>
          <th>Stats:</th>
        </tr>
      </thead>
      <tbody id="flashcard-sets-container"></tbody>
    </table>
    <script>
      document.getElementById("form").onsubmit = (function(event) {
        event.preventDefault();
        var searchTerm = document.getElementById("search-bar").value;
        document.getElementById("flashcard-sets-container").innerHTML = '';
        fetch("https://csa-backend.rohanj.dev/api/flashcard/getFlashcardSetsByName", {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({name: searchTerm})
        }).then(data => data.json())
          .then(data => {
            data.forEach(data => {
              var flashcardSetRow = document.createElement("tr");
              var flashcardSetElem = document.createElement("td");
              var flashcardSetName = document.createElement("p");
              flashcardSetName.innerHTML = data.name;
              flashcardSetElem.appendChild(flashcardSetName);
              flashcardSetRow.appendChild(flashcardSetElem);
              document.getElementById("flashcard-sets-container").appendChild(flashcardSetRow);
              // fetch stats from backend for this flashcard set
              fetch("https://csa-backend.rohanj.dev/api/stats/getStatsByFlashcardSetId", {
                method: 'POST',
                headers: {
                  'Content-Type': 'application/json'
                },
                body: JSON.stringify({flashcardSetId: data.id})
              }).then(statsData => statsData.json())
                .then(statsData => {
                  var statsElem = document.createElement("td");
                  if (statsData.length > 0) {
                    var stats = statsData[0];
                    var statsText = "Total Quiz Attempts: " + stats.totalQuizAttempts + ", Total Flashcard Views: " + stats.totalFlashcardViews;
                    statsElem.innerHTML = statsText;
                  } else {
                    statsElem.innerHTML = "No stats available";
                  }
                  flashcardSetRow.appendChild(statsElem);
                });
            });
          });
      });
    </script>
  </body>
</html>
