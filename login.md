## Log In

<!--No actions yet-->


<table>
    <tr>
        <td>Email:</td>
        <td><input type="email" id="email" name="email" required></td>
    </tr>
    <tr>
        <td>Password:</td>
        <td><input type="text" id="password" name="password" required></td>
    </tr>
    <tr>
        <td><button type="submit" value="Submit" onclick="login_user()">Submit</button></td>
    </tr>
</table>
<h4>Don't have an account? Sign up <a href="/signup">here</a></h4>

<script>
    // Replace with localhost:8085 for testing
    

    var url = "https://csa-backend.rohanj.dev/api/login/authenticate";
    
    function login_user() {
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
                response.text().then(data => {
                    console.log(data);
                    document.cookie = "token=" + data;
                    //window.location.href = "/team-8-frontend/search";
                })
            })
            .catch(err => {
                console.log("Error: " + err);
            })
    }


</script>