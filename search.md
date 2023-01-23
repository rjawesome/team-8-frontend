<h1>Flashcard Search</h1>
  <form>
    <label for="search-bar">Search for Flashcard Sets:</label>
    <input type="text" id="search-bar" name="search-bar">
    <br>
    <label for="class-filter">Filter by Class:</label>
    <select id="class-filter" name="class-filter">
      <option value="all">All Classes</option>
      <option value="AP Physics">AP Physics</option>
      <option value="AP Calculus">AP Calculus</option>
      <option value="AP US History">AP US History</option>
    </select>
    <br><br>
    <input type="submit" value="Search">
  </form>
  <script>
    // add event listener for form submission
    document.querySelector("form").addEventListener("submit", function(event) {
      event.preventDefault();
      var searchTerm = document.getElementById("search-bar").value;
      var classFilter = document.getElementById("class-filter").value;
      console.log("Searching for flashcard sets with the term: " + searchTerm + " and class filter: " + classFilter);
      // send searchTerm and classFilter to server or perform search logic here
    });
  </script>