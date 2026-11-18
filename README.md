
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<h1>Happy 11th Monthsary, Steffy! 💗</h1>
<p>Welcome to your special little adventure!</p>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  background: #fff0f5;
  color: #a7476c;
  font-family: Georgia, serif;
  text-align: center;
}

header {
  padding: 65px 20px;
  background: linear-gradient(135deg,#ffb9d0,#fff0f5);
}

h1 { font-size: 38px; }
h2 { color: #c0527b; }

section { padding: 40px 18px; }

button {
  background: #e77da1;
  color: white;
  border: none;
  padding: 13px 22px;
  border-radius: 25px;
  margin: 7px;
  cursor: pointer;
  font-size: 15px;
  transition: .25s;
}

button:hover {
  background: #c0527b;
  transform: scale(1.05);
}

.card {
  background: white;
  max-width: 550px;
  padding: 25px;
  margin: 20px auto;
  border-radius: 20px;
  box-shadow: 0 5px 18px #e9bdce;
}

.hidden { display: none !important; }

.hearts {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 12px;
  max-width: 500px;
  margin: 25px auto;
}

.heart {
  background: white;
  border-radius: 15px;
  padding: 20px 5px;
  font-size: 32px;
  cursor: pointer;
  box-shadow: 0 3px 10px #e9bdce;
}

.heart p {
  font-size: 11px;
  margin: 5px 0 0;
}

.quiz-option {
  display: block;
  width: 100%;
  max-width: 330px;
  margin: 10px auto;
}

.progress {
  height: 12px;
  background: #f4ccda;
  border-radius: 20px;
  max-width: 400px;
  margin: 15px auto;
  overflow: hidden;
}

#bar {
  height: 100%;
  width: 0%;
  background: #e77da1;
  transition: .3s;
}

#memoryGrid {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 10px;
  max-width: 400px;
  margin: 20px auto;
}

.memory-card {
  height: 75px;
  border-radius: 12px;
  background: #f6b6ce;
  font-size: 28px;
  cursor: pointer;
}

.memory-card:disabled {
  background: white;
  cursor: default;
}

#finalGift {
  font-size: 85px;
  cursor: pointer;
}

footer {
  padding: 25px;
  background: #ffc4d8;
}

</style>
</head>

<body>

<header>
  <h1>Our Little Love Adventure 💗</h1>
  <p>11 months, 11 hearts, and countless memories.</p>
  <p>A special game made just for you!</p>
  <button onclick="startGame()">START OUR ADVENTURE 💌</button>
</header>

<div id="game" class="hidden">

  <section>
    <h2>🎮 Your Mission</h2>
    <div class="card">
      <p>Welcome, my favorite person!</p>
      <p>Complete these three little challenges to unlock your special surprise.</p>
      <p>💗 Find 11 hearts</p>
      <p>💕 Answer the couple quiz</p>
      <p>🧩 Complete the memory game</p>
      <div class="progress">
        <div id="bar"></div>
      </div>
      <p id="progressText">0 / 3 challenges completed</p>
    </div>
  </section>

  <section>
    <h2>💗 Challenge 1: Find the 11 Hearts</h2>
    <p>Click every heart to reveal a reason why I love you!</p>

    <div class="hearts" id="hearts"></div>
    <p id="heartCount">0 / 11 hearts discovered</p>
  </section>

  <section>
    <h2>💕 Challenge 2: Couple Quiz</h2>

    <div class="card">
      <h3 id="question">Question 1</h3>
      <div id="answers"></div>
      <p id="quizFeedback"></p>
      <p id="quizCount">Question 1 of 3</p>
    </div>
  </section>

  <section>
    <h2>🧩 Challenge 3: Memory Match</h2>
    <p>Find all the matching pairs!</p>

    <div id="memoryGrid"></div>
    <p id="memoryStatus">0 / 4 pairs found</p>
  </section>

  <section id="surprise" class="hidden">
    <h2>🎉 YOU DID IT!</h2>
    <div class="card">
      <h2>All Challenges Completed! 💗</h2>
      <p>You unlocked your final surprise!</p>
      <div id="finalGift" onclick="revealFinal()">🎁</div>
      <p>Tap your gift to open it!</p>
      <div id="finalMessage" class="hidden">
        <h1>💖</h1>
        <h2>Happy 11th Monthsary My Babbyyy!</h2>
        <p>
          Thank you for playing my little game.
          But the biggest prize isn't the game...
          it's having you in my life.
        </p>
        <p>
          Thank you for these 11 wonderful months.
          Here's to more laughter, memories,
          adventures, and love.
        </p>
        <h2>I LOVE YOU! ❤️</h2>
        <p>Forever your favorite person.</p>
      </div>
    </div>
  </section>

</div>

<footer>
  <p>Made with love, just for you. 💗</p>
  <p>Our 11th Monthsary ❤️</p>
  
<section>
  <h2>🎵 Our Special Song</h2>

  <div class="card">
    <h3>There Is a Light That Never Goes Out</h3>
    <p>By The Smiths ❤️</p>

    <audio controls loop>
      <source src="music.mp3" type="audio/mpeg">
      Your browser does not support audio.
    </audio>

    <p><small>A little soundtrack for our special day.</small></p>
  </div>
</section>

</footer>

<script>

// EDIT YOUR 11 REASONS HERE
const reasons = [
  "Your beautiful smile",
  "Your kindness",
  "Your funny jokes",
  "Your personality",
  "Your patience",
  "The way you care",
  "Your support",
  "Our conversations",
  "Our beautiful memories",
  "The happiness you bring",
  "Simply because you're YOU!"
];

// EDIT YOUR QUIZ QUESTIONS HERE

const questions = [
  {
    question: "What special occasion are we celebrating?",
    answers: ["Birthday 🎂", "11th Monthsary ❤️", "Christmas 🎄"],
    correct: 1
  },
  {
    question: "How many months have we been together?",
    answers: ["5 months", "11 months", "1 month"],
    correct: 1
  },
  {
    question: "What nickname is on this website?",
    answers: ["Steffy", "Baby Bear", "Honey"],
    correct: 0
  },
  {
    question: "How many hearts are waiting for you?",
    answers: ["5", "10", "11"],
    correct: 2
  },
  {
    question: "How many main challenges are in this game?",
    answers: ["2", "3", "5"],
    correct: 1
  },
  {
    question: "What happens after completing all challenges?",
    answers: ["You unlock a gift", "The game disappears", "Nothing"],
    correct: 0
  },
  {
    question: "What makes a relationship stronger?",
    answers: ["Trust", "Lying", "Ignoring each other"],
    correct: 0
  },
  {
    question: "What should couples practice?",
    answers: ["Communication", "Silent treatment", "Avoiding problems"],
    correct: 0
  },
  {
    question: "What is important when making promises?",
    answers: ["Breaking them", "Keeping them", "Forgetting them"],
    correct: 1
  },
  {
    question: "What should you do after a misunderstanding?",
    answers: ["Talk calmly", "Ignore everything", "Start an argument"],
    correct: 0
  },
  {
    question: "What makes someone feel appreciated?",
    answers: ["Kindness", "Disrespect", "Being ignored"],
    correct: 0
  },
  {
    question: "What is a good way to show love?",
    answers: ["Through actions", "Through lies", "Through arguments"],
    correct: 0
  },
  {
    question: "What should you do when your partner is sad?",
    answers: ["Listen and support", "Laugh at them", "Ignore them"],
    correct: 0
  },
  {
    question: "What makes a good relationship?",
    answers: ["Mutual respect", "Controlling each other", "Constant arguments"],
    correct: 0
  },
  {
    question: "What should couples do when they disagree?",
    answers: ["Listen to each other", "Insult each other", "Never communicate"],
    correct: 0
  },
  {
    question: "What is more meaningful?",
    answers: ["Thoughtful gestures", "Expensive things only", "Showing off"],
    correct: 0
  },
  {
    question: "What helps build trust?",
    answers: ["Honesty", "Secrets and lies", "Broken promises"],
    correct: 0
  },
  {
    question: "What is quality time?",
    answers: ["Giving each other attention", "Ignoring each other", "Always being distracted"],
    correct: 0
  },
  {
    question: "What should partners support?",
    answers: ["Each other's dreams", "Each other's failures", "Unhealthy habits"],
    correct: 0
  },
  {
    question: "What is a healthy way to handle mistakes?",
    answers: ["Admit and learn", "Blame everyone", "Pretend nothing happened"],
    correct: 0
  },
  {
    question: "What makes memories special?",
    answers: ["The moments we share", "The price of things", "Other people's opinions"],
    correct: 0
  },
  {
    question: "What should you do when your partner needs space?",
    answers: ["Respect their space", "Get angry", "Demand attention"],
    correct: 0
  },
  {
    question: "What is important besides saying 'I love you'?",
    answers: ["Showing care", "Making excuses", "Ignoring feelings"],
    correct: 0
  },
  {
    question: "What makes a relationship a team?",
    answers: ["Working together", "Competing against each other", "Keeping score"],
    correct: 0
  },
  {
    question: "What should you do when your partner achieves something?",
    answers: ["Celebrate with them", "Make them feel bad", "Ignore it"],
    correct: 0
  },
  {
    question: "What is a good way to solve a problem?",
    answers: ["Listen and cooperate", "Shout louder", "Avoid the issue forever"],
    correct: 0
  },
  {
    question: "What should you remember during difficult days?",
    answers: ["Be patient and understanding", "Give up immediately", "Stop communicating"],
    correct: 0
  },
  {
    question: "What makes little surprises special?",
    answers: ["The thought behind them", "Their price", "Their size"],
    correct: 0
  },
  {
    question: "What should both people contribute to a relationship?",
    answers: ["Effort and respect", "Only demands", "Only expectations"],
    correct: 0
  },
  {
    question: "What is this website's biggest purpose?",
    answers: ["To celebrate our 11th monthsary", "To teach mathematics", "To sell something"],
    correct: 0
  }
];
  
let foundHearts = 0;
let quizIndex = 0;
let quizScore = 0;
let quizCompleted = false;
let memoryCompleted = false;
let completedPairs = 0;

function startGame() {
  document.getElementById("game").classList.remove("hidden");
  document.getElementById("game").scrollIntoView({
    behavior: "smooth"
  });
}

// HEART CHALLENGE
const heartContainer = document.getElementById("hearts");

reasons.forEach((reason,index) => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = `💗<p>Heart ${index+1}</p>`;

  heart.onclick = () => {
    if(heart.dataset.opened) return;

    heart.dataset.opened = "yes";
    heart.innerHTML = `❤️<p>${reason}</p>`;
    heart.style.background = "#ffe0eb";

    foundHearts++;
    document.getElementById("heartCount").innerText =
      foundHearts + " / 11 hearts discovered";

    if(foundHearts === 11) {
      heartContainer.style.opacity = "1";
      updateProgress();
    }
  };

  heartContainer.appendChild(heart);
});

// QUIZ CHALLENGE

function showQuestion() {
  if(quizIndex >= questions.length) {
    document.getElementById("question").innerText =
      "Quiz completed! 🎉";

    document.getElementById("answers").innerHTML = "";

    document.getElementById("quizFeedback").innerHTML =
      "Your final score: " + quizScore + " / 30 💗";

    document.getElementById("quizCount").innerText =
      "30 / 30 questions completed";

    quizCompleted = true;
    updateProgress();
    return;
  }

  const q = questions[quizIndex];

  document.getElementById("question").innerText =
    "Question " + (quizIndex + 1) + ": " + q.question;

  document.getElementById("quizCount").innerText =
    "Question " + (quizIndex + 1) + " of 30";

  document.getElementById("quizFeedback").innerText = "";

  const answers = document.getElementById("answers");
  answers.innerHTML = "";

  q.answers.forEach((answer,index) => {
    const button = document.createElement("button");
    button.className = "quiz-option";
    button.innerText = answer;

    button.onclick = () => {
      if(index === q.correct) {
        quizScore++;

        document.getElementById("quizFeedback").innerText =
          "Correct! You're amazing, Steffy Babyy! 💖";

        answers.innerHTML = "";

        quizIndex++;
        setTimeout(showQuestion, 900);
      } else {
        document.getElementById("quizFeedback").innerText =
          "Oops! Try again, Babbyy! 💗";
      }
    };

    answers.appendChild(button);
  });
}

  const q = questions[quizIndex];

  document.getElementById("question").innerText = q.question;
  document.getElementById("quizCount").innerText =
    `Question ${quizIndex+1} of ${questions.length}`;

  document.getElementById("quizFeedback").innerText = "";

  const answers = document.getElementById("answers");
  answers.innerHTML = "";

  q.answers.forEach((answer,index) => {
    const button = document.createElement("button");
    button.className = "quiz-option";
    button.innerText = answer;

    button.onclick = () => {
      if(index === q.correct) {
        document.getElementById("quizFeedback").innerText =
          "Correct! You're doing great! 💖";

        quizIndex++;
        setTimeout(showQuestion,900);
      } else {
        document.getElementById("quizFeedback").innerText =
          "Not quite! Try again! 💗";
      }
    };

    answers.appendChild(button);
  });
}

showQuestion();

// MEMORY GAME
let symbols = ["🌸","🌸","💗","💗","🐻","🐻","🎀","🎀"];
let firstCard = null;
let secondCard = null;
let lockBoard = false;

symbols.sort(() => Math.random() - 0.5);

const memoryGrid = document.getElementById("memoryGrid");

symbols.forEach(symbol => {
  const card = document.createElement("button");
  card.className = "memory-card";
  card.innerText = "❔";
  card.dataset.symbol = symbol;

  card.onclick = () => {
    if(lockBoard || card.disabled || card === firstCard) return;

    card.innerText = symbol;

    if(!firstCard) {
      firstCard = card;
      return;
    }

    secondCard = card;
    lockBoard = true;

    if(firstCard.dataset.symbol === secondCard.dataset.symbol) {
      firstCard.disabled = true;
      secondCard.disabled = true;
      completedPairs++;

      document.getElementById("memoryStatus").innerText =
        completedPairs + " / 4 pairs found";

      resetCards();

      if(completedPairs === 4) {
        memoryCompleted = true;
        updateProgress();
      }
    } else {
      setTimeout(() => {
        firstCard.innerText = "❔";
        secondCard.innerText = "❔";
        resetCards();
      },800);
    }
  };

  memoryGrid.appendChild(card);
});

function resetCards() {
  firstCard = null;
  secondCard = null;
  lockBoard = false;
}

// PROGRESS
function updateProgress() {
  const completed = [
    foundHearts === 11,
    quizCompleted,
    memoryCompleted
  ].filter(Boolean).length;

  document.getElementById("bar").style.width =
    (completed / 3 * 100) + "%";

  document.getElementById("progressText").innerText =
    completed + " / 3 challenges completed";

  if(completed === 3) {
    document.getElementById("surprise").classList.remove("hidden");
    document.getElementById("surprise").scrollIntoView({
      behavior: "smooth"
    });
  }
}

// FINAL GIFT
function revealFinal() {
  document.getElementById("finalMessage").classList.remove("hidden");
  document.getElementById("finalGift").innerText = "💝";
}

</script>
</body>
</html>
