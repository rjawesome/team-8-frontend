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

<button onclick="getYearInfo">Get Year Info</button>
<button onclick="getDayInfo">Get Day Info</button>
<button onclick="getLeapYears">Find Number of Leap Years</button>
<button onclick="getYearFact">Get Year Fact</button>

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
        var url = "https://backend-csa.rohanj.dev/calendar1/yearInfo/" + Document.getElementById("year1").innerHTML;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.body.innerHTML += table;
            })
        })

        .catch(err => {
            Document.getElementById("result").innerHTML = "Error: " + err;
        })

        }

    function getDayInfo() {
        var url = "https://backend-csa.rohanj.dev/calendar1/dayInfo/" + Document.getElementById("day").innerHTML;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.body.innerHTML += table;
            })
        })

        .catch(err => {
            Document.getElementById("result").innerHTML = "Error: " + err;
        })
    }

    function getLeapYears() {
        var url = "https://backend-csa.rohanj.dev/calendar1/leapYears/" + Document.getElementById("year1").innerHTML + "/" + Document.getElementById("year2").innerHTML;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.body.innerHTML += table;
            })
        })

        .catch(err => {
            Document.getElementById("result").innerHTML = "Error: " + err;
        })
    }

    function getYearFact() {
        var url = "https://backend-csa.rohanj.dev/calendar2/" + Document.getElementById("year1").innerHTML;

        fetch(url, options).then(response => {

            response.json().then(data => {
                var table = "<table>"
                for (var key in data) {
                if (data.hasOwnProperty(key)) {
                    table += '<tr><td>' + key + '</td><td>' + data[key] + '</td></tr>';
                    }
                }
            table += '</table>';
            document.body.innerHTML += table;
            })
        })

        .catch(err => {
            Document.getElementById("result").innerHTML = "Error: " + err;
        })
    }
</script>