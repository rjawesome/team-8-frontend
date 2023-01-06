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

<input type="button" onClick="getYearInfo()">Get Year Info</input>
<input type="button" onClick="getDayInfo()">Get Day Info</input>
<input type="button" onClick="getLeapYears()">Find Number of Leap Years</input>
<input type="button" onClick="getYearFact()">Get Year Fact</input>

<label id="result"></label>

<script>

    function getYearInfo() {
        String link = "https://backend-csa.rohanj.dev/calendar1/" + Document.getElementById("year1");
        fetch(link, {})
    }

    function getDayInfo() {

    }

    function getLeapYears() {

    }

    function getYearFact() {

    }
</script>