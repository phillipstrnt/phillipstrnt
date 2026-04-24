# 👋 Hi, I'm Phillip

🚀 Aspiring Full-Stack Developer | Turning Ideas into Reality

---

## 🧑‍💻 About Me
- 💻 Passionate about **web & mobile development**
- 📚 Learning **JavaScript, React, Node.js & MongoDB**
- ⚡ Exploring **Kotlin**
- 🎯 Goal: Become a **professional full-stack developer**
- 🔥 Consistency > Motivation

---

## 🚀 Tech Stack

### 💻 Languages
![JavaScript](https://img.shields.io/badge/JavaScript-yellow?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-orange?style=for-the-badge&logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-blue?style=for-the-badge&logo=css3)
![Kotlin](https://img.shields.io/badge/Kotlin-purple?style=for-the-badge&logo=kotlin)

### ⚙️ Frameworks & Libraries
![React](https://img.shields.io/badge/React-blue?style=for-the-badge&logo=react)
![Node.js](https://img.shields.io/badge/Node.js-green?style=for-the-badge&logo=node.js)
![Express](https://img.shields.io/badge/Express-black?style=for-the-badge&logo=express)

### 🗄️ Database
![MongoDB](https://img.shields.io/badge/MongoDB-darkgreen?style=for-the-badge&logo=mongodb)

### 🔧 Tools
![Git](https://img.shields.io/badge/Git-black?style=for-the-badge&logo=git)
![GitHub](https://img.shields.io/badge/GitHub-gray?style=for-the-badge&logo=github)
![VS Code](https://img.shields.io/badge/VSCode-blue?style=for-the-badge&logo=visual-studio-code)

---

## 📊 Skill Progress
JavaScript ██████████░░ 80%  
React ████████░░░░ 70%  
Node.js ███████░░░░░ 65%  
MongoDB ██████░░░░░░ 60%  
Kotlin █████░░░░░░░ 50%

---

## 📚 Currently Learning
![TypeScript](https://img.shields.io/badge/TypeScript-blue?style=for-the-badge&logo=typescript)
![Next.js](https://img.shields.io/badge/Next.js-black?style=for-the-badge&logo=next.js)

---

## 📊 GitHub Stats
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=tokyonight"/>
</p>

---

## 📌 Top Languages
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=tokyonight"/>
</p>

---

## 🐍 Contribution Snake
<!-- <p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake.svg"/>
</p> -->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Snake Game</title>

<style>
    body {
        margin: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background: #111;
        font-family: Arial;
        color: white;
    }

    canvas {
        background: #222;
        border: 3px solid #0f0;
    }

    .score {
        position: absolute;
        top: 20px;
        font-size: 20px;
    }
</style>
</head>

<body>

<div class="score">Score: <span id="score">0</span></div>
<canvas id="game" width="400" height="400"></canvas>

<script>
const canvas = document.getElementById("game");
const ctx = canvas.getContext("2d");

const scoreDisplay = document.getElementById("score");

const box = 20;

let snake = [{ x: 9 * box, y: 10 * box }];

let direction = "RIGHT";

let food = {
    x: Math.floor(Math.random() * 19) * box,
    y: Math.floor(Math.random() * 19) * box
};

let score = 0;

// Controls
document.addEventListener("keydown", changeDirection);

function changeDirection(event) {
    let key = event.keyCode;

    if (key == 37 && direction != "RIGHT") direction = "LEFT";
    else if (key == 38 && direction != "DOWN") direction = "UP";
    else if (key == 39 && direction != "LEFT") direction = "RIGHT";
    else if (key == 40 && direction != "UP") direction = "DOWN";
}

// Collision check
function collision(head, array) {
    for (let i = 0; i < array.length; i++) {
        if (head.x == array[i].x && head.y == array[i].y) {
            return true;
        }
    }
    return false;
}

// Draw game
function draw() {
    ctx.fillStyle = "#222";
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    // Snake
    for (let i = 0; i < snake.length; i++) {
        ctx.fillStyle = i == 0 ? "lime" : "green";
        ctx.fillRect(snake[i].x, snake[i].y, box, box);
    }

    // Food
    ctx.fillStyle = "red";
    ctx.fillRect(food.x, food.y, box, box);

    // Old head position
    let snakeX = snake[0].x;
    let snakeY = snake[0].y;

    // Direction movement
    if (direction == "LEFT") snakeX -= box;
    if (direction == "RIGHT") snakeX += box;
    if (direction == "UP") snakeY -= box;
    if (direction == "DOWN") snakeY += box;

    // Eat food
    if (snakeX == food.x && snakeY == food.y) {
        score++;
        scoreDisplay.innerText = score;

        food = {
            x: Math.floor(Math.random() * 19) * box,
            y: Math.floor(Math.random() * 19) * box
        };
    } else {
        snake.pop();
    }

    // New head
    let newHead = { x: snakeX, y: snakeY };

    // Game over conditions
    if (
        snakeX < 0 ||
        snakeY < 0 ||
        snakeX >= canvas.width ||
        snakeY >= canvas.height ||
        collision(newHead, snake)
    ) {
        clearInterval(game);
        alert("Game Over 💀 Score: " + score);
    }

    snake.unshift(newHead);
}

let game = setInterval(draw, 100);
</script>

</body>
</html>

---

## 🔥 What I'm Working On
- 🚧 Full-stack projects
- 🌍 Real-world solutions
- 🧠 Clean code & problem solving

---

## 🤝 Connect With Me
- 📧 Email: phillipstrnt@gmail.com  
- 💼 LinkedIn: YOUR_LINK  

---

⭐ Code. Learn. Build. Repeat.
