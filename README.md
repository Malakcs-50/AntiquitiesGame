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

    background:black;

}

.portalContainer{

    text-align:center;

    color:white;

}

.portalImage{

    width:280px;

    animation:spin 5s linear infinite;

}

@keyframes spin{

    from{
        transform:rotate(0deg);
    }

    to{
        transform:rotate(360deg);
    }

}

h1{

    color:gold;

    margin-top:25px;

    font-size:42px;

}

p{

    margin-top:20px;

    font-size:22px;

    line-height:35px;

}

button{

    margin-top:35px;

    padding:15px 35px;

    border:none;

    border-radius:10px;

    background:gold;

    font-size:20px;

    cursor:pointer;

    transition:.3s;

}

button:hover{

    transform:scale(1.05);

}
