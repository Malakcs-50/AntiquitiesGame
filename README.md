let selectedCharacter = "";

const boy = document.getElementById("boy");
const girl = document.getElementById("girl");
const startBtn = document.getElementById("startBtn");
const playerName = document.getElementById("playerName");

boy.addEventListener("click", function () {

    selectedCharacter = "boy";

    boy.classList.add("selected");
    girl.classList.remove("selected");

});

girl.addEventListener("click", function () {

    selectedCharacter = "girl";

    girl.classList.add("selected");
    boy.classList.remove("selected");

});

startBtn.addEventListener("click", function () {

    const name = playerName.value.trim();

    if (name === "") {
        alert("Please enter your name.");
        return;
    }

    if (selectedCharacter === "") {
        alert("Please choose a character.");
        return;
    }

    localStorage.setItem("playerName", name);
    localStorage.setItem("character", selectedCharacter);

    window.location.href = "story.html";

});
