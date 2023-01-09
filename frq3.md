## FRQ 3: Calculator

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
    fetch(`${API_URL}${encodeURIComponent(expression)}`)
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