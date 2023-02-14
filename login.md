## Log In

<!--No actions yet-->

<form onsubmit="login_user()" method="post" id="form" autocomplete="on">
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
            <td><input type="submit" value="Submit"></td>
        </tr>
    </table>
</form>
<h4>Don't have an account? Sign up <a href="/signup">here</a></h4>

<script>
    // Replace with localhost:8085 for testing
    //var url = "csa-backend.rohanj.dev";
    var url = "localhost:8085";

    const login_url = "http://" + url + "/api/jwt/authenticate";
    
    function login_user() {
        const body = {

            // Should be same as person????
            email: document.getElementById("email").value,
            password: document.getElementById("password").value
        };
        const request_options = {
            method: "POST",
            mode: "cors",
            cache: "no-cache",
            credentials: "include",
            body: JSON.stringify(body),
            headers: {
                "content-type": "application/json"
            }
        };
        fetch(login_url, request_options)
            .then(response => {
                if (!response.ok) {
                    const errorMsg = "Login error: " + response.status;
                    console.log(errorMsg);
                    return;
                }
                window.location.href = "/team-8-frontend/search";
            })
    }


</script>