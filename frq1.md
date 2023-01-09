## FRQ 1: Calendar

> API to get some information about a year

<label for="fname">Year 1:</label>
<input type="text" id="year1" name="year1"><br><br>
<label for="lname">Year 2:</label>
<input type="text" id="year2" name="year2"><br><br>
<label for="fname">Month:</label>
<input type="text" id="month" name="month"><br><br>
<label for="lname">Day:</label>
<input type="text" id="day" name="day"><br><br>

<br><br>

<button onclick="getYearInfo()">Get Year Info</button>
<button onclick="getDayInfo()">Get Day Info</button>
<button onclick="getLeapYears()">Find Number of Leap Years</button>
<button onclick="getYearFact()">Get Year Fact</button>

<label id="result"></label>

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
        var url = "https://csa-backend.rohanj.dev/api/calendar1/dayInfo/" + document.getElementById("day").value + "/" + document.getElementById("month").value + document.getElementById("year1").value;

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
        var url = "https://csa-backend.rohanj.dev/api/calendar2/" + document.getElementById("year1").value;

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