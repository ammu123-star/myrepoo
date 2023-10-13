<!DOCTYPE html>
<html>

<head>
    <meta name="viewport" content="width-device-width, initial- scale=1.0">
    <title>Login Authentication</title>
</head>

<style>
    * {
        margin: 0;
        padding: 0;
        font-family: Algerian;
        color:black;
        box-sizing: border-box;
    }

    .container {
        width: 100%;
        height: 100vh;
        background:url("login.webp");
        background-size: cover;
        
        position: relative;

    }

    .form-box {
        width: 100%;
        max-width: 500px;
        max-height:600px;
        position: absolute;
        top: 50%;
        left: 700px;
        transform: translate(-50%, -50%);
        background:grey;
        opacity:0.7;
        padding: 50px 60px 70px;
        text-align: center;
        justify-content: center;

    }

    .form-box h1 {
        font-size: 40px;
        position: relative;
        margin-bottom: 60px;
    }

    .form-box h1::after {
        content: ' ';
        width: 30px;
        height: 4px;
        border-radius: 3px;
        background: black;
        position: absolute;
        bottom: -12px;
        left: 65%;
        transform: translate(-50px);
    }

    .input-field {
        background: white;
        margin: 15px 0;
        border-radius: 3px;
        display: flex;
        align-items: center;
        max-height: 65px;
        transition: max-height 0.5s;
        overflow: hidden;
    }

    input {
        width: 90%;
        background: transparent;
        border: black;
        outline: 0;
        padding: 18px 15px;
    }

    .input-field i {
        margin-left: 15px;
        color: black;
    }

    form p {
        text-align: center;
        font-size: 13px;
    }

    form p a {
        text-decoration: none;
        color: black;
    }

    .btn-field {
        width: 100%;
        display: flex;
        justify-content: space-between;
    }

    .btn-field button {
        flex-basis: 48%;
        background:black;
        height: 35px;
        border-radius: 20px;
        border: 0;
        outline: 0;
        color: white;
    }
.btn-field .disable{
    background: white;
    color: black;
}
    
</style>

<body>
    <div class="container">
        <div class="form-box">
            <h1 id="tittle"> Sign Up</h1>
            <form>
                <div classs="input-group">
                    <div class="input-field" id="nameField">
                        <i class="fa-solid fa-user"></i>

                        <input type="text" placeholder="Name" required>
                    </div>
                    <div class="input-field">
                        <i class="fa-regular fa-envelope"></i>
                        <input type="email" placeholder="Email" required>
                    </div>
                    <div class="input-field">
                        <i class="fa-solid fa-lock"></i>
                        <input type="password" placeholder="Password" required>
                    </div>
                    <p>forget password <a href="#">Click Here!</a></p><br>
                </div>
                <div class="btn-field">
                    <button type="button" id="signupBtn">Sign up</button>
                    <button type="button" id="signinBtn" class="disable">Sign in</button>
                </div>
            </form>

        </div>
    </div>

<script>
    let signupBtn = document.getElementById("signupBtn");
    let signinBtn = document.getElementById("signinBtn");
    let nameField = document.getElementById("nameField");
    let tittle = document.getElementById("tittle");



    signinBtn.onclick = function(){
        nameField.style.maxHeight="0";
        tittle.innerHTML="Sign In";
        signupBtn.classList.add("disable");
        signinBtn.classList.remove("disable");
 }
 signupBtn.onclick = function(){
    nameField.style.maxHeight = "65px";
    tittle.innerHTML = "Sign up";
    signupBtn.classList.remove("disable");
    signinBtn.classList.add("disable");
 }

</script>


</body>

</html>
