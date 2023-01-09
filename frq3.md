## FRQ 3: Calculator

<form id="calculator-form">
  <label for="expression-input">Expression:</label><br>
  <input type="text" id="expression-input" name="expression"><br>
  <button type="submit" id="submit-button">Submit</button>
</form> 
<br/>

<table id="results-table">
  <tr>
    <th>Expression</th>
    <th> <strong> Answer </strong> </th>
  </tr>
</table>

<style>
.button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
}

  .button2:hover {
  box-shadow: 0 12px 16px 0 rgba(201,242,155),0 17px 50px 0 rgba(0,0,0,0.19)
}

input[type=text] {
  border: 4px solid green;
  border-radius: 4px;
}

input[type=submit] {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  -webkit-transition-duration: 0.4s; /* Safari */
  transition-duration: 0.4s;
}

.label {
  color: lime;
}

</style>

<script>
  // checks rohan juneja's api
  const API_URL = 'https://csa-backend.rohanj.dev/api/calculator1/calculate?expression=';
  document.getElementById('calculator-form').addEventListener('submit', (event) => {
    event.preventDefault();
    let expression = document.getElementById('expression-input').value;
    expression = expression.replace(/\^/g, 'POW');
    fetch(`${API_URL}${encodeURIComponent(expression)}`)
      .then(response => response.json())
      .then(data => {
        const table = document.getElementById('results-table');
        const row = table.insertRow(-1);
        const expressionCell = row.insertCell(0);
        const resultCell = row.insertCell(1);
        expressionCell.innerHTML = expression;
        resultCell.innerHTML = `<strong>${data}</strong>`;
      });
  });
</script>