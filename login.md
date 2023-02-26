## Log In

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
        <td><button onclick="login_user()" id="submit" type="submit" value="Submit">Submit</button></td> 
        <!-- onclick="login_user()" -->
        <!-- ngl onclick sucks ass-->
    </tr>
</table>
<h4>Don't have an account? Sign up <a href="/signup">here</a></h4>

<script>
    
    // Replace with localhost:8085 for testing

    var test_url = "http://localhost:8085/api/jwt/authenticate";

    var url = "https://csa-backend.rohanj.dev/api/login/authenticate";
    var responsey = undefined;
    
    // function login_user() {
    //     const body = {

    //         // Should be same as person????
    //         email: document.getElementById("email").value,
    //         password: document.getElementById("password").value
    //     };
    //     const request_options = {
    //         method: 'POST',
    //         body: JSON.stringify(body),
    //         headers: {
    //             "content-type": 'application/json'
    //         }
    //     };
    //     console.log(JSON.stringify(body));


    //     fetch(url, request_options)
    //         .then(response => {
    //             response.text().then(data => {
    //                 console.log(data);
    //                 document.cookie = "token=" + data;
    //                 //window.location.href = "/team-8-frontend/search";
    //             })
    //         })
    //         .catch(err => {
    //             console.log("Error: " + err);
    //         })
    // }

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
                "content-type": 'application/json'
            },
            credentials: 'include'
        };
        fetch(url, request_options)
            .then(response => {
                if (response.status != 200) {
                    alert("Error Occured: Please check your email and password")
                    return
                }
                alert("logged in!")
                responsey = response
                console.log(response)
                window.location.href = "/yourflashcardsets"
            })
            .catch(err => {
                console.log("Error: " + err);
            })
    }

</script>
