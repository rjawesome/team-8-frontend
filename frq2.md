## FRQ 2: Steptrack

# Create User
<form action="https://csa-backend.rohanj.dev/api/steptrack1/createPerson" method="post" id="form">
  <table>
    <tr>
      <td>Age:</td>
      <td><input type="number" name="age" required></td>
    </tr>
    <tr>
      <td>Name:</td>
      <td><input type="text" name="name" required></td>
    </tr>
    <tr>
      <td>Email:</td>
      <td><input type="email" name="email" required></td>
    </tr>
    <tr>
      <td>Gender:</td>
      <td><input type="text" name="gender" required></td>
    </tr>
    <tr>
      <td>Height (in):</td>
      <td><input type="number" name="heightIn" required></td>
    </tr>
    <tr>
      <td>Weight (lbs):</td>
      <td><input type="number" name="weightLbs" required></td>
    </tr>
  </table>
  <input type="submit" value="Submit">
</form>

<script>
    var form = document.getElementById("form")
    form.onsubmit = (event) => {
        event.preventDefault();
        var obj = {};
        for (var i of Object.values(form.elements)) {
            if (i.type === "number") {
                obj[i.name] = i.valueAsNumber;
            } else {
                obj[i.name] = i.value;
            }
        }
        console.log(obj)

        var xhr = new XMLHttpRequest();
        xhr.open('POST', 'https://csa-backend.rohanj.dev/api/steptrack1/createPerson', true);
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.onload = function () {
          if (xhr.status === 201) {
            // If the request was successful, create an HTML table with the response data
            var response = JSON.parse(xhr.responseText);
            console.log(response);
            var table = '<table>';
            for (var key in response) {
              if (response.hasOwnProperty(key)) {
                table += '<tr><td>' + key + '</td><td>' + response[key] + '</td></tr>';
              }
            }
            table += '</table>';
            document.body.innerHTML += table;
          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send(obj);
    }
</script>