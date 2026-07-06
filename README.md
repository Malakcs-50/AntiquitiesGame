*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    overflow:hidden;
    background:#111;
}

#welcome{
    width:100%;
    height:100vh;
    background:url("images/museum.jpg");
    background-size:cover;
    background-position:center;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
}

.overlay{
    position:absolute;
    width:100%;
    height:100%;
    background:rgba(0,0,0,.6);
}

.card{
    position:relative;
    z-index:10;
    width:450px;
    padding:40px;
    background:rgba(255,255,255,.1);
    backdrop-filter:blur(10px);
    border-radius:20px;
    text-align:center;
    color:white;
    border:1px solid rgba(255,255,255,.2);
    box-shadow:0 15px 35px rgba(0,0,0,.5);
}

.logo{
    width:120px;
    margin-bottom:20px;
}

h1{
    color:gold;
    margin-bottom:15px;
    font-size:40px;
}

p{
    margin-bottom:25px;
    line-height:28px;
}

input{
    width:100%;
    padding:15px;
    border:none;
    border-radius:10px;
    margin-bottom:25px;
    font-size:16px;
}

h2{
    margin-bottom:20px;
}

.characters{
    display:flex;
    justify-content:space-around;
    margin-bottom:30px;
}

.character{
    width:130px;
    height:150px;
    object-fit:cover;
    border-radius:15px;
    cursor:pointer;
    transition:.3s;
}

.character:hover{
    transform:scale(1.05);
}

.selected{
    border:5px solid gold;
}

button{
    width:100%;
    padding:15px;
    border:none;
    border-radius:10px;
    background:gold;
    color:black;
    font-size:18px;
    font-weight:bold;
    cursor:pointer;
    transition:.3s;
}

button:hover{
    background:#ffd700;
    transform:scale(1.03);
}
