/*body{

margin:0;

display:flex;

justify-content:center;

align-items:center;

background:#222;

}

.museum{

position:relative;

width:900px;

}

.museumImage{

width:100%;

display:block;

}

.era{

position:absolute;

cursor:pointer;

}

/* الفرعوني */

/*#s1{

left:180px;
top:145px;

width:540px;
height:95px;

}

/* اليوناني */

/*#s2{

left:180px;
top:245px;

width:540px;
height:100px;

}

/* القبطي */

/*#s3{

left:180px;
top:350px;

width:260px;
height:90px;

}

/* الآثار الغارقة */

/*#s4{

left:450px;
top:350px;

width:270px;
height:90px;

}

/* الإسلامي */

/*#s5{

left:180px;
top:445px;

width:540px;
height:100px;

}

.locked{

background:rgba(0,0,0,.5);

}

.unlocked{

background:rgba(255,215,0,.25);

}

.unlocked:hover{

border:4px solid gold;

}*/





*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    margin:0;
    overflow:hidden;
    background:#000;
}

.museum{
    position:relative;
    width:100vw;
    height:100vh;
}

.museumImage{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
}

/* جميع مناطق الضغط */
.era{
    position:absolute;
    cursor:pointer;
    transition:.3s;
}

.era:hover{
    transform:scale(1.03);
}

/* العصر الفرعوني */
#s1{
    left:24%;
    top:21%;
    width:56%;
    height:12%;
}

/* العصر اليوناني */
#s2{
    left:24%;
    top:38%;
    width:56%;
    height:12%;
}

/* العصر القبطي */
#s3{
    left:24%;
    top:55%;
    width:27%;
    height:12%;
}

/* الآثار الغارقة */
#s4{
    left:53%;
    top:55%;
    width:27%;
    height:12%;
}

/* العصر الإسلامي */
#s5{
    left:24%;
    top:72%;
    width:56%;
    height:12%;
}

/* المراحل المقفولة */
.locked{
    background:rgba(0,0,0,.45);
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:50px;
    color:white;
}

/* المراحل المفتوحة */
.unlocked{
    background:rgba(255,215,0,.2);
}

.unlocked:hover{
    border:4px solid gold;
    box-shadow:0 0 20px gold;
}
