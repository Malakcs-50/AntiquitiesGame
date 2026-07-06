const player = localStorage.getItem("playerName");

const text = document.getElementById("storyText");
const button = document.getElementById("nextBtn");

const story =
`Welcome ${player}...

You have discovered a mysterious museum.

A hidden Time Portal has awakened.

The timeline has been broken.

Collect the Five Time Keys.

Restore history before it disappears forever.`;

let i = 0;

function typing(){

    if(i < story.length){

        text.innerHTML += story.charAt(i);

        i++;

        setTimeout(typing,40);

    }else{

        button.style.display="inline-block";

    }

}

typing();

button.onclick=function(){

    window.location.href="portal.html";

};
