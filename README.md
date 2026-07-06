<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Victory</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{

    background:black;

    height:100vh;

    display:flex;

    justify-content:center;

    align-items:center;

    flex-direction:column;

    color:white;

    text-align:center;

}

img{

    width:250px;

    margin-bottom:20px;

}

h1{

    color:gold;

    margin-bottom:15px;

}

h2{

    margin-bottom:20px;

}

p{

    font-size:22px;

    margin-bottom:20px;

}

button{

    padding:15px 35px;

    background:gold;

    color:black;

    border:none;

    border-radius:10px;

    cursor:pointer;

    font-size:18px;

}

button:hover{

    transform:scale(1.05);

}

</style>

</head>

<body>

<img src="images/portal.png" alt="Portal">

<h1>🏺 Guardian Of History 🏺</h1>

<h2 id="player"></h2>

<p>
You collected all Time Keys and restored history.
</p>

<p id="finalScore"></p>

<button onclick="location.href='index.html'">
Play Again
</button>

<script>

document.getElementById("player").textContent =
localStorage.getItem("playerName");

document.getElementById("finalScore").textContent =
"Final Score : " + localStorage.getItem("finalScore");

</script>

</body>

</html>
