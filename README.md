const level = Number(localStorage.getItem("currentLevel")) || 1;
let score = Number(localStorage.getItem("score")) || 0;

const data = {

1:{
title:"🏺 Ancient Egyptian Era",

questions:[

{
image:"images/artifact1.jpg",
story:"The Rosetta Stone helped historians understand hieroglyphics.",
question:"Why is the Rosetta Stone important?",
answers:[
"It helped read hieroglyphics",
"It built pyramids",
"It was a temple",
"It was a crown"
],
correct:0
},

{
image:"images/artifact2.jpg",
story:"Tutankhamun was one of Egypt's most famous kings.",
question:"Who owned this artifact?",
answers:[
"Khufu",
"Tutankhamun",
"Cleopatra",
"Ramses"
],
correct:1
},

{
image:"images/artifact3.jpg",
story:"The Great Pyramid is one of the Seven Wonders.",
question:"Who built the Great Pyramid?",
answers:[
"Khufu",
"Menes",
"Ramses",
"Akhenaten"
],
correct:0
}

]

},

2:{
title:"🏛 Greek Era",

questions:[

{
image:"images/greek1.jpg",
story:"The Greeks built many beautiful temples.",
question:"Who was the king of the gods?",
answers:[
"Zeus",
"Apollo",
"Hades",
"Ares"
],
correct:0
},

{
image:"images/greek2.jpg",
story:"The Parthenon is in Athens.",
question:"Where is the Parthenon?",
answers:[
"Rome",
"Athens",
"Cairo",
"Paris"
],
correct:1
},

{
image:"images/greek3.jpg",
story:"Greek statues were famous for realism.",
question:"What were Greek statues famous for?",
answers:[
"Gold",
"Realism",
"Glass",
"Wood"
],
correct:1
}

]

},

3:{
title:"⛪ Coptic Era",

questions:[

{
image:"images/coptic1.jpg",
story:"The Hanging Church is one of Egypt's oldest churches.",
question:"Where is the Hanging Church?",
answers:[
"Cairo",
"Alexandria",
"Luxor",
"Aswan"
],
correct:0
},

{
image:"images/coptic2.jpg",
story:"Coptic art often shows saints.",
question:"What does Coptic art usually show?",
answers:[
"Saints",
"Cars",
"Animals",
"Ships"
],
correct:0
},

{
image:"images/coptic3.jpg",
story:"The Coptic language comes from Ancient Egyptian.",
question:"The Coptic language developed from?",
answers:[
"Greek",
"Ancient Egyptian",
"Arabic",
"Latin"
],
correct:1
}

]

},
4:{
title:"🌊 Underwater Antiquities",

questions:[

{
image:"images/water1.jpg",
story:"Many ancient cities were submerged under the sea.",
question:"Where are underwater antiquities found?",
answers:[
"Deserts",
"Sea",
"Mountains",
"Forests"
],
correct:1
},

{
image:"images/water2.jpg",
story:"Divers discovered many ancient statues.",
question:"Who discovered these statues?",
answers:[
"Pilots",
"Divers",
"Drivers",
"Doctors"
],
correct:1
},

{
image:"images/water3.jpg",
story:"Some underwater ruins are near Alexandria.",
question:"Which city is famous for underwater ruins?",
answers:[
"Giza",
"Alexandria",
"Aswan",
"Luxor"
],
correct:1
}

]

},

5:{
title:"🕌 Islamic Era",

questions:[

{
image:"images/islamic1.jpg",
story:"Islamic architecture is famous for beautiful mosques.",
question:"Which building represents Islamic architecture?",
answers:[
"Mosque",
"Pyramid",
"Temple",
"Castle"
],
correct:0
},

{
image:"images/islamic2.jpg",
story:"Arabic calligraphy decorated Islamic buildings.",
question:"What decorated Islamic buildings?",
answers:[
"Paint",
"Calligraphy",
"Plastic",
"Glass"
],
correct:1
},

{
image:"images/islamic3.jpg",
story:"Many mosques have beautiful domes.",
question:"What is common in Islamic mosques?",
answers:[
"Domes",
"Snow",
"Bridges",
"Towers"
],
correct:0
}

]

}

};

const quiz = data[level];

let current = 0;

const title = document.getElementById("levelTitle");
const image = document.getElementById("artifactImage");
const story = document.getElementById("artifactStory");
const question = document.getElementById("question");
const buttons = document.querySelectorAll(".answer");
const scoreText = document.getElementById("score");

function loadQuestion(){

const q = quiz.questions[current];

title.textContent = quiz.title;
image.src = q.image;
story.textContent = q.story;
question.textContent = q.question;

buttons.forEach((button,index)=>{
button.textContent = q.answers[index];
});

scoreText.textContent = "Score : " + score;

}

buttons.forEach((button,index)=>{

button.onclick = function(){

if(index === quiz.questions[current].correct){

score += 10;
alert("✅ Correct!");

}else{

alert("❌ Wrong!");

}

current++;

if(current >= quiz.questions.length){

finishLevel();
return;

}

loadQuestion();

};

});

loadQuestion();

function finishLevel(){

localStorage.setItem("score",score);

if(level < 5){

localStorage.setItem("level",level + 1);

alert("🎉 Era Completed!");

window.location.href = "map.html";

}else{

localStorage.setItem("finalScore",score);

window.location.href = "win.html";

}

}
