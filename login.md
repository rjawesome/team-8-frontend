## Log In

<!--No actions yet-->

<!--Replace post with csa-backend.rohanj.dev/authenticate later, testing with localhost for now-->
<form action="localhost:8085/api/jwt/authenticate" method="post" id="form" autocomplete="on">
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
            <td><input type="submit" value="Submit"></td>
        </tr>
    </table>
</form>
<h4>Don't have an account? Sign up <a href="/signup">here</a></h4>