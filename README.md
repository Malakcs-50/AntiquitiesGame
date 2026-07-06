*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{

background:url("images/museum.jpg");
background-size:cover;
display:flex;
justify-content:center;
align-items:center;
height:100vh;

}

.quizBox{

width:900px;
padding:30px;
background:rgba(0,0,0,.85);
border:3px solid gold;
border-radius:20px;
text-align:center;
color:white;

}

#levelTitle{

color:gold;
margin-bottom:20px;

}

#artifactImage{

width:350px;
height:250px;
object-fit:cover;
border-radius:15px;
border:3px solid gold;

}

#artifactStory{

margin:20px 0;
font-size:20px;

}

#question{

margin-bottom:25px;
color:gold;

}

.answers{

display:grid;
grid-template-columns:1fr 1fr;
gap:15px;

}

.answer{

padding:15px;
background:gold;
border:none;
border-radius:10px;
cursor:pointer;
font-size:18px;

}

.answer:hover{

background:white;

}

#score{

margin-top:25px;
font-size:24px;
color:gold;

}
