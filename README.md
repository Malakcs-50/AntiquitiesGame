<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Echoes Of Time</title>

    <link rel="stylesheet" href="style.css">
</head>

<body>

    <section id="welcome">

        <div class="overlay"></div>

        <div class="card">

            <img src="images/logo.gif" class="logo" alt="Logo">

            <h1>Echoes Of Time</h1>

            <p>
                Welcome to the Antiquities Museum.
                <br>
                Start your journey through time.
            </p>

            <input
                type="text"
                id="playerName"
                placeholder="Enter Your Name">

            <h2>Choose Character</h2>

            <div class="characters">

                <img src="images/boy.jpeg"
                     id="boy"
                     class="character"
                     alt="Boy">

                <img src="images/girl.png"
                     id="girl"
                     class="character"
                     alt="Girl">

            </div>

            <button id="startBtn">
                START ADVENTURE
            </button>

        </div>

    </section>

    <script src="script.js"></script>

</body>

</html>
