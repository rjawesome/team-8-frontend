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
    }
</script>