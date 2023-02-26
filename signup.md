## Sign Up

<!--No actions yet-->


<table>
    <tr>
        <td>Email:</td>
        <td><input type="email" id="email" name="email" required></td>
    </tr>
    <tr>
        <td>Password:</td>
        <td><input type="password" id="password" name="password" required></td>
    </tr>
    <tr>
        <td><button type="submit" value="Submit" onclick="create_user()">Submit</button></td>
    </tr>
</table>
<h4>Have an account? Log in <a href="/login">here</a></h4>

<script>
    // Replace with localhost:8085 for testing
    

    var url = "https://csa-backend.rohanj.dev/api/user/createPerson";
    
    function create_user() {
        const body = {

            // Should be same as person????
            email: document.getElementById("email").value,
            password: document.getElementById("password").value
        };
        const request_options = {
            method: 'POST',
            body: JSON.stringify(body),
            headers: {
                "content-type": 'application/json'
            }
        };
        console.log(JSON.stringify(body));


        fetch(url, request_options)
            .then(response => {
                response.json().then(data => {
                    if (data.err) {
                       alert(data.err)
                    } else {
                       alert("Account created! Please enter your credentials to log in.")
                       window.location.href = "/login";
                    }
                })
            })
            .catch(err => {
                console.log("Error: " + err);
            })
    }


</script>
