## FRQ 3: Calculator

<form id="calculator-form">
  <label for="expression-input">Expression:</label><br>
  <input type="text" id="expression-input" name="expression"><br>
  <button type="submit" id="submit-button">Submit</button>
</form> 

<br/>


<h1>Calculator</h1>

<input id="expression" type="text">
<button id="submit">Get Result!</button>
<p id="output"></p>

<script>
document.getElementById("submit").onclick = () => {
	fetch("http://localhost:8085/api/calculator1/calculate?expression=" + encodeURIComponent(document.getElementById("expression").value)).then(body => body.text()).then(body => {
    document.getElementById("output").innerHTML = body;
  })
}
</script>
