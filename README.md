let level = localStorage.getItem("level");

if(level==null){

level=1;

localStorage.setItem("level",1);

}

for(let i=2;i<=5;i++){

if(level>=i){

document.getElementById("s"+i).classList.remove("locked");

document.getElementById("s"+i).classList.add("unlocked");

document.getElementById("s"+i).onclick=function(){

openQuiz(i);

}

}

}

function openQuiz(level){

    localStorage.setItem("currentLevel", level);

    window.location.href = "quiz.html";

}

