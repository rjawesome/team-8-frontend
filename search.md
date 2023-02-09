<h2>Flashcard Search</h2>
  <form id="form">
    <label for="search-bar">Search for Flashcard Sets:</label>
    <input type="text" id="search-bar" name="search-bar">
    <br>
    <!-- <label for="class-filter">Filter by Class:</label>
    <select id="class-filter" name="class-filter">
      <option value="all">All Classes</option>
      <option value="AP Physics">AP Physics</option>
      <option value="AP Calculus">AP Calculus</option>
      <option value="AP US History">AP US History</option>
    </select> -->
    <br><br>
    <input type="submit" value="Search">
  </form>
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
          console.log(data.name)
        })
      });
      })
    </script>