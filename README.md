const questions = [

{
image:"images/artifact1.jpg",

story:
"The Rosetta Stone helped historians understand Ancient Egyptian hieroglyphics.",

question:
"Why is the Rosetta Stone important?",

answers:[
"It helped read hieroglyphics",
"It built pyramids",
"It was a crown",
"It was a temple"
],

correct:0
},

{
image:"images/artifact2.jpg",

story:
"This artifact belonged to Tutankhamun, one of the most famous Pharaohs.",

question:
"Who owned this artifact?",

answers:[
"Khufu",
"Ramses",
"Tutankhamun",
"Cleopatra"
],

correct:2
},

{
image:"images/artifact3.jpg",

story:
"The Great Pyramid of Giza is one of the Seven Wonders of the Ancient World.",

question:
"Who built the Great Pyramid?",

answers:[
"Khufu",
"Menes",
"Ramses",
"Akhenaten"
],

correct:0
},

{
image:"images/statue.jpg",

story:
"Ancient Egyptian statues were created to honor kings and gods.",

question:
"Why were these statues built?",

answers:[
"To honor Pharaohs",
"To play games",
"To build houses",
"To make food"
],

correct:0
},

{
image:"images/museum-front.jpg",

story:
"The Antiquities Museum preserves priceless pieces of history.",

question:
"What is the purpose of a museum?",

answers:[
"Preserve history",
"Sell food",
"Build roads",
"Make phones"
],

correct:0
}

];

let currentQuestion = 0;
let score = 0;
let keys = 0;

const image =
document.getElementById("artifactImage");

const story =
document.getElementById("artifactStory");

const question =
document.getElementById("question");

const questionNumber =
document.getElementById("questionNumber");

const scoreText =
document.getElementById("score");

const keysText =
document.getElementById("keys");

const buttons =
document.querySelectorAll(".answer");

function loadQuestion(){

    const q = questions[currentQuestion];

    image.src = q.image;

    story.innerHTML = q.story;

    question.innerHTML = q.question;

    questionNumber.innerHTML =
    "Question " +
    (currentQuestion + 1) +
    " / " +
    questions.length;

    buttons.forEach((button,index)=>{

        button.innerHTML =
        q.answers[index];

    });

    scoreText.innerHTML =
    "Score : " + score;

    keysText.innerHTML =
    "🔑 " + keys + " / 5";
}

loadQuestion();

buttons.forEach((button,index)=>{

    button.onclick = function(){

        if(index === questions[currentQuestion].correct){

            score += 10;

            keys++;

            alert("✅ Correct! You found a Time Key.");

        }else{

            alert("❌ Wrong Answer.");
        }

        currentQuestion++;

        if(currentQuestion >= questions.length){

            localStorage.setItem(
                "finalScore",
                score
            );

            window.location.href =
            "win.html";

            return;
        }

        loadQuestion();
    };
});
