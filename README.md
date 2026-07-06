*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:url("images/museum.jpg");
    background-size:cover;
    background-position:center;
}

.storyBox{
    width:700px;
    max-width:90%;
    background:rgba(0,0,0,.75);
    padding:40px;
    border-radius:20px;
    text-align:center;
    color:white;
    border:2px solid gold;
}

h1{
    color:gold;
    margin-bottom:25px;
}

#storyText{
    font-size:22px;
    line-height:38px;
    min-height:220px;
    white-space:pre-line;
}

button{
    margin-top:30px;
    padding:15px 35px;
    font-size:18px;
    background:gold;
    color:black;
    border:none;
    border-radius:10px;
    cursor:pointer;
    transition:.3s;
}

button:hover{
    transform:scale(1.05);
}
