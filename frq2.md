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
      <td>Password:</td>
      <td><input type="text" name="password" required></td>
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

<h6>result: </h6>
<p id="result"></P>

# Get User
<form action="https://csa-backend.rohanj.dev/api/steptrack1/getUser" method="post" id="formGetUser">
  <table>
    <tr>
      <td>Email:</td>
      <td><input type="email" name="email" required></td>
    </tr>
    <tr>
      <td>Password:</td>
      <td><input type="text" name="password" required></td>
    </tr>
  </table>
  <input type="submit" value="Submit">
</form>

<h6>result: </h6>
<div id="resultGetUser"></div>

# Delete User
<form action="https://csa-backend.rohanj.dev/api/steptrack1/deletePerson" method="delete" id="formDeletePerson">
  <table>
    <tr>
      <td>Email:</td>
      <td><input type="email" name="email" required></td>
    </tr>
    <tr>
      <td>Password:</td>
      <td><input type="text" name="password" required></td>
    </tr>
  </table>
  <input type="submit" value="Submit">
</form>

<h6>result: </h6>
<p id="resultDeletePerson"></p>


# Set Stats
<form action="https://csa-backend.rohanj.dev/api/steptrack1/setStats" method="post" id="formSetStats">
  <table>
    <tr>
      <td>Email:</td>
      <td><input type="email" name="email" required></td>
    </tr>
    <tr>
      <td>Password:</td>
      <td><input type="text" name="password" required></td>
    </tr>
    <tr>
      <td>Steps:</td>
      <td><input type="number" name="steps" required></td>
    </tr>
    <tr>
      <td>Calories:</td>
      <td><input type="number" name="calories" required></td>
    </tr>
    <tr>
      <td>Day:</td>
      <td><input type="number" name="day" required></td>
    </tr>
    <tr>
      <td>Month:</td>
      <td><input type="number" name="month" required></td>
    </tr>
    <tr>
      <td>Year:</td>
      <td><input type="number" name="year" required></td>
    </tr>
  </table>
  <input type="submit" value="Submit">
</form>

<h6>result: </h6>
<div id="resultSetStats"></div>

# Get Stats
<form action="https://csa-backend.rohanj.dev/api/steptrack1/getStats" method="post" id="formSetStats">
  <table>
    <tr>
      <td>Email:</td>
      <td><input type="email" name="email" required></td>
    </tr>
    <tr>
      <td>Password:</td>
      <td><input type="text" name="password" required></td>
    </tr>
    <tr>
      <td>Day:</td>
      <td><input type="number" name="day" required></td>
    </tr>
    <tr>
      <td>Month:</td>
      <td><input type="number" name="month" required></td>
    </tr>
    <tr>
      <td>Year:</td>
      <td><input type="number" name="year" required></td>
    </tr>
  </table>
  <input type="submit" value="Submit">
</form>

<h6>result: </h6>
<div id="resultSetStats"></div>

<script>
  function inputAsJson(id) {
    var form = document.getElementById(id)
      var obj = {};
        for (var i of Object.values(form.elements)) {
            if (i.type === "number") {
                obj[i.name] = i.valueAsNumber;
            } else {
                obj[i.name] = i.value;
            }
        }
        console.log(obj)
        return obj;
  }

// createUser
    var form = document.getElementById("form")
    form.onsubmit = (event) => {
        event.preventDefault();
        var obj = inputAsJson("form");

        var xhr = new XMLHttpRequest();
        xhr.open('POST', 'https://csa-backend.rohanj.dev/api/steptrack1/createPerson', true);
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.onload = function () {
          if (xhr.status === 201) {
            // If the request was successful, create an HTML table with the response data
            var response = xhr.responseText;
            console.log(response);
            var result = document.getElementById("result");
            result.innerHTML = response;
          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send(JSON.stringify(obj));
    }

// getUser
    var getUser = document.getElementById("formGetUser")
    getUser.onsubmit = (event) => {
      event.preventDefault();
      var obj = inputAsJson("formGetUser");
      console.log(JSON.stringify(obj));
      var xhr = new XMLHttpRequest();
        xhr.open('POST', 'https://csa-backend.rohanj.dev/api/steptrack1/getPerson');
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.onload = function () {
          if (xhr.status === 200) {
            var result = document.getElementById("resultGetUser");
            var response = JSON.parse(xhr.responseText);
            var table = '<table>';
            for (var key in response) {
              if (response.hasOwnProperty(key)) {
                table += '<tr><td>' + key + '</td><td>' + response[key] + '</td></tr>';
              }
            }
            table += '</table>';
            result.innerHTML = table;
          } else {
            // If the request was unsuccessful, display an error message
            console.log(xhr.status)
          }
        };
        xhr.send(JSON.stringify(obj));
    }

    // deleteUser
    var form = document.getElementById("formDeletePerson")
    form.onsubmit = (event) => {
        event.preventDefault();
        var obj = inputAsJson("formDeletePerson");

        var xhr = new XMLHttpRequest();
        xhr.open('DELETE', 'https://csa-backend.rohanj.dev/api/steptrack1/deletePerson', true);
        xhr.setRequestHeader('Content-Type', 'application/json');
        
        xhr.setRequestHeader('Access-Control-Allow-Methods', 'DELETE, POST');
        xhr.onload = function () {
          if (xhr.status === 200) {
            // If the request was successful, create an HTML table with the response data
            var response = xhr.responseText;
            console.log(response);
            var result = document.getElementById("resultDeletePerson");
            result.innerHTML = response;
          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send(JSON.stringify(obj));
    }

    // setStats
    var setStats = document.getElementById("formSetStats")
    setStats.onsubmit = (event) => {
        event.preventDefault();
        var obj = inputAsJson("formSetStats");
        console.log(JSON.stringify(obj));
        var xhr = new XMLHttpRequest();
        xhr.open('POST', 'https://csa-backend.rohanj.dev/api/steptrack1/setStats', true);
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.onload = function () {
          if (xhr.status === 200) {
            // If the request was successful, create an HTML table with the response data
            var result = document.getElementById("resultSetStats");
            var response = JSON.parse(xhr.responseText);
            var table = '<table>';
            for (var key in response) {
              if (response.hasOwnProperty(key)) {
                table += '<tr><td>' + key + '</td><td>' + response[key] + '</td></tr>';
              }
            }
            table += '</table>';
            result.innerHTML = table;
          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send(JSON.stringify(obj));
    }

    // getStats
    var getStats = document.getElementById("formGetStats")
    getStats.onsubmit = (event) => {
        event.preventDefault();
        var obj = inputAsJson("formGetStats");
        console.log(JSON.stringify(obj));
        var xhr = new XMLHttpRequest();
        xhr.open('POST', 'https://csa-backend.rohanj.dev/api/steptrack1/getStats', true);
        xhr.setRequestHeader('Content-Type', 'application/json');
        xhr.onload = function () {
          if (xhr.status === 200) {
            // If the request was successful, create an HTML table with the response data
            var result = document.getElementById("resultGetStats");
            var response = JSON.parse(xhr.responseText);
            var table = '<table>';
            for (var key in response) {
              if (response.hasOwnProperty(key)) {
                table += '<tr><td>' + key + '</td><td>' + response[key] + '</td></tr>';
              }
            }
            table += '</table>';
            result.innerHTML = table;
          } else {
            // If the request was unsuccessful, display an error message
            alert('Request failed. Returned status of ' + xhr.status);
          }
        };
        xhr.send(JSON.stringify(obj));
    }
</script>