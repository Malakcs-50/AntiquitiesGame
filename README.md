*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    overflow:hidden;
}

.background{

    width:100%;
    height:100vh;

    background:url("images/museum.jpg");

    background-size:cover;
    background-position:center;

}

.overlay{

    width:100%;
    height:100%;

    background:rgba(0,0,0,.75);

    display:flex;

    justify-content:center;

    align-items:center;

}

#storyBox{

    width:700px;

    text-align:center;

    color:white;

}

#title{

    font-size:55px;

    color:#D4AF37;

    margin-bottom:40px;

}

#storyText{

    font-size:28px;

    line-height:55px;

    min-height:220px;

}

#nextBtn{

    margin-top:40px;

    padding:18px 50px;

    font-size:22px;

    border:none;

    border-radius:10px;

    background:#D4AF37;

    color:white;

    cursor:pointer;

    display:none;

}

#nextBtn:hover{

    background:#b89120;

}
