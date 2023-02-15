<link rel="stylesheet" href="{{ '/assets/css/search.scss?v=' | append: site.github.build_revision | relative_url }}">
<html>
  <head>
    <title>Flashcard Stats</title>
  </head>
  <body>
    <h2>Flashcard Statistics</h2>
    <h3 id="flashcardset-name"></h3>
    <table>
      <thead>
        <tr>
          <th>Front</th>
          <th>Back</th>
          <th>Correct</th>
          <th>Incorrect</th>
        </tr>
      </thead>
      <tbody id="stats-table-body"></tbody>
    </table>
  
  <script>
      const statsTableBody = document.getElementById('stats-table-body');
      var currentUrl = window.location.href;
      let url = new URL(currentUrl);                                                  
      let urlParams = new URLSearchParams(url.search); 


      const ID = parseInt(urlParams.get('id')); // will be inputted by user later
      if (ID === null || isNaN(ID)) {
        window.location.pathname = "/search.html";
      }

      fetch("https://csa-backend.rohanj.dev/api/flashcard/getFlashcardSet",
        { 
          method: 'POST',  
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({id: ID})
        }
      ).then(response => {
        response.json().then(data => {
          document.getElementById("flashcardset-name").innerText = data.meta.name;
        });
      });

      fetch('https://csa-backend.rohanj.dev/api/stats/getStatsByFlashcardSet',{ 
        method: 'POST',  
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify({email: "rohanj2006@gmail.com", password: "password", id: 20})
      })
        .then(response => response.json())
        .then(stats => {
          stats.forEach(stat => {
            const row = document.createElement('tr');
            const flashcardFront = document.createElement('td');
            const flashcardBack = document.createElement('td');
            const correctCell = document.createElement('td');
            const incorrectCell = document.createElement('td');
            
            flashcardFront.innerText = stat.flashcard.front;
            flashcardBack.innerText = stat.flashcard.back;
            correctCell.innerText = stat.correct;
            incorrectCell.innerText = stat.incorrect;

            row.appendChild(flashcardFront);
            row.appendChild(flashcardBack);
            row.appendChild(correctCell);
            row.appendChild(incorrectCell);

            statsTableBody.appendChild(row);
          });
      });
    </script>
  </body>
</html>
