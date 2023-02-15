
<html>
  <head>
    <meta charset="UTF-8">
    <title>Flashcard Statistics</title>
  </head>
  <body>
    <h2>Flashcard Statistics</h2>
    <table>
      <thead>
        <tr>
          <th>Flashcard Set</th>
          <th>Flashcard</th>
          <th>Correct</th>
          <th>Incorrect</th>
        </tr>
      </thead>
      <tbody id="stats-table-body">
      </tbody>
    </table>
  
  <script>
      const statsTableBody = document.getElementById('stats-table-body');
      fetch('https://csa-backend.rohanj.dev/stats')
        .then(response => response.json())
        .then(stats => {
          stats.forEach(stat => {
            const row = document.createElement('tr');
            const flashcardSetCell = document.createElement('td');
            const flashcardCell = document.createElement('td');
            const correctCell = document.createElement('td');
            const incorrectCell = document.createElement('td');
            
            flashcardSetCell.innerText = stat.flashcardSet.name;
            flashcardCell.innerText = stat.flashcard.question;
            correctCell.innerText = stat.correct;
            incorrectCell.innerText = stat.incorrect;

            row.appendChild(flashcardSetCell);
            row.appendChild(flashcardCell);
            row.appendChild(correctCell);
            row.appendChild(incorrectCell);

            statsTableBody.appendChild(row);
          });
        })
        .catch(error => {
          console.error('Failed to fetch flashcard statistics', error);
        });
    </script>
  </body>
</html>
