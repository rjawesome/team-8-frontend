## FRQ 1: Calendar

> API to get some information about a year

<label color="lime" for="fname">Year 1:</label>
<input type="text" id="year1" name="year1"><br><br>
<label color="lime" for="lname">Year 2:</label>
<input type="text" id="year2" name="year2"><br><br>
<label color="lime" for="fname">Month:</label>
<input type="text" id="month" name="month"><br><br>
<label color="lime" for="lname">Day:</label>
<input type="text" id="day" name="day"><br><br>

<br><br>

<button class="button button2" onclick="getYearInfo()">Get Year Info</button>
<button class="button button2" onclick="getDayInfo()">Get Day Info</button>
<button class="button button2" onclick="getLeapYears()">Find Number of Leap Years</button>
<button class="button button2" onclick="getYearFact()">Get Year Fact</button>

<label id="result"></label>

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
  border: 2px solid green;
  border-radius: 4px;
}

</style>

<script>

    const options = {
            method: 'GET', // *GET, POST, PUT, DELETE, etc.
            mode: 'cors', // no-cors, *cors, same-origin
            cache: 'default', // *default, no-cache, reload, force-cache, only-if-cached
            credentials: 'omit', // include, *same-origin, omit
            headers: {
            'Content-Type': 'application/json'
            // 'Content-Type': 'application/x-www-form-urlencoded',
            },
        };
    
    function getYearInfo() {
        var url = "https://csa-backend.rohanj.dev/api/calendar1/yearInfo/" + document.getElementById("year1").value;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.getElementById("result").innerHTML = table;
            })
        })

        .catch(err => {
            document.getElementById("result").innerHTML = "Error: " + err;
        })

        }

    function getDayInfo() {
        var url = "https://csa-backend.rohanj.dev/api/calendar1/dayInfo/" + document.getElementById("day").value + "/" + document.getElementById("month").value + "/" + document.getElementById("year1").value;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.getElementById("result").innerHTML = table;
            })
        })

        .catch(err => {
            document.getElementById("result").innerHTML = "Error: " + err;
        })
    }

    function getLeapYears() {
        var url = "https://csa-backend.rohanj.dev/api/calendar1/leapYears/" + document.getElementById("year1").value + "/" + document.getElementById("year2").value;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
           document.getElementById("result").innerHTML = table;
            })
        })

        .catch(err => {
            document.getElementById("result").innerHTML = "Error: " + err;
        })
    }

    function getYearFact() {
        var url = "https://csa-backend.rohanj.dev/api/calendar2/yearFact" + document.getElementById("year1").value;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.getElementById("result").innerHTML = table;
            })
        })

        .catch(err => {
            document.getElementById("result").innerHTML = "Error: " + err;
        })
    }
</script>