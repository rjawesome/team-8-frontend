## FRQ 3: Calculator

<form id="calculator-form">
  <label for="expression-input">Expression:</label><br>
  <input type="text" id="expression-input" name="expression"><br>
  <button type="submit" id="submit-button">Submit</button>
</form> 

<br/>

<h1>Calculator</h1>

<table id="results-table">
  <tr>
    <th>Expression</th>
    <th>Tokens</th> 
    <th>RPN</th>
    <th> <strong> Answer </strong> </th>
  </tr>
</table>

<script>
  // checks rohan juneja's api
  const API_URL = 'https://csa-backend.rohanj.dev/api/calculator1/calculate?expression=';
  document.getElementById('calculator-form').addEventListener('submit', (event) => {
    event.preventDefault();
    let expression = document.getElementById('expression-input').value;
    expression = expression.replace(/\^/g, 'POW');
    fetch(`${API_URL}expression=${expression}`)
      .then(response => response.json())
      .then(data => {
        const table = document.getElementById('results-table');
        const row = table.insertRow(-1);
        const expressionCell = row.insertCell(0);
        const tokensCell = row.insertCell(1);
        const rpnCell = row.insertCell(2);
        const resultCell = row.insertCell(3);
        expressionCell.innerHTML = data.Expression;
        tokensCell.innerHTML = data.Tokens;
        rpnCell.innerHTML = data.RPN;
        resultCell.innerHTML = `<strong>${data.Result}</strong>`;
      });
  });
</script>


<h1>Calculator</h1>

<input id="expression" type="text">
<button id="submit">Get Result!</button>
<p id="output"></p>

<script>
document.getElementById("submit").onclick = () => {
	fetch("https://csa-backend.rohanj.dev/api/calculator1/calculate?expression=" + encodeURIComponent(document.getElementById("expression").value)).then(body => body.text()).then(body => {
    document.getElementById("output").innerHTML = body;
  })
}
</script>
