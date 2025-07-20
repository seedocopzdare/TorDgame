<!DOCTYPE html>
<html lang="ml">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dangerous Romantic Truth or Dare - 2 Player</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffcccc, #ffe6e6);
      color: #333;
      text-align: center;
      padding: 20px;
      animation: fadeIn 2s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    h1 {
      color: #e6005c;
      animation: popIn 1.5s ease;
    }
    @keyframes popIn {
      0% { transform: scale(0.5); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }
    .player {
      font-size: 20px;
      font-weight: bold;
      margin-top: 20px;
    }
    .question-box {
      background-color: #fff0f5;
      border: 2px dashed #e6005c;
      border-radius: 20px;
      padding: 20px;
      margin: 20px auto;
      width: 80%;
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0% { box-shadow: 0 0 0 0 rgba(230, 0, 92, 0.7); }
      70% { box-shadow: 0 0 0 20px rgba(230, 0, 92, 0); }
      100% { box-shadow: 0 0 0 0 rgba(230, 0, 92, 0); }
    }
    button {
      padding: 10px 20px;
      font-size: 18px;
      background-color: #e6005c;
      color: white;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      margin: 10px;
      transition: transform 0.2s;
    }
    button:hover {
      background-color: #cc0052;
      transform: scale(1.05);
    }
  </style>
</head>
<body>
  <h1>🌹 Dangerous Romantic Truth or Dare 🌹</h1>
  <div class="player">ഇപ്പോൾ കളിക്കുന്നവൻ: <span id="currentPlayer">Player 1</span></div>
  <div class="question-box" id="questionBox">👇 ഒരു ചോദ്യത്തിനായി ബട്ടൺ അമർത്തൂ 👇</div>
  <button onclick="nextQuestion()">Next Question</button>
  <button onclick="switchPlayer()">Switch Player</button>
  <br>
  <button onclick="shareWhatsApp()">📤 WhatsApp-ൽ ഷെയർ ചെയ്യൂ</button>

  <script>
    const questions = [
      "ഒരു ഇമോഷ്യണൽ സീക്രട്ട് പറഞ്ഞു തരൂ 😌",
      "നിനക്ക് ഏറ്റവും wild ആയ सपना എന്താണ്?",
      "ഒരു ചില്ലറ കിസ്സിന്റെ അനുഭവം വെളിപ്പെടുത്തൂ 😳",
      "ഒരിക്കൽ നീ കാണാനാഗ്രഹിക്കുന്ന dangerous fantasy എന്താണ്?",
      "പ്ലേയറുടെ ഓർമയിൽ നിൽക്കുന്ന ഒറ്റ കിടിലൻ പുണ്യപ്രവൃത്തി പറയൂ 😈",
      "ഇന്നത്തെ രാത്രിക്ക് ഒരു title കൊടുത്താൽ? 😏",
      "നിന്റെ body-ൽ ഏറ്റവും sensitive spot? 😉",
      "Player 2-നെ കുറിച്ച് സത്യം പറയൂ (Cute ആകട്ടേ) ❤️",
      "ഒരിക്കൽ dare ചെയ്യാനാവാത്തതായത് എന്താണ്?",
      "നിന്റെ ലവ്-ലിസ്റ്റിൽ ഒറ്റ dangerous move? 💋",
      // Add more up to 200 questions for better experience
    ];

    while (questions.length < 200) {
      questions.push("Random സത്യവും ഡെയറും, നീ ഒരുക്കെ ആകണം 😜");
    }

    let currentPlayer = 1;
    function nextQuestion() {
      const index = Math.floor(Math.random() * questions.length);
      const qBox = document.getElementById("questionBox");
      qBox.innerHTML = `<strong>${questions[index]}</strong>`;
    }

    function switchPlayer() {
      currentPlayer = currentPlayer === 1 ? 2 : 1;
      document.getElementById("currentPlayer").textContent = `Player ${currentPlayer}`;
      document.getElementById("questionBox").textContent = "👇 ഇനി ചോദ്യമാക്കൂ 👇";
    }

    function shareWhatsApp() {
      const message = `🌹 Dangerous Romantic Truth or Dare 🌹\n\nPlayer ${currentPlayer} ന്റെ ടേൺ!\n\n👉 https://your-game-link-here.html`;
      const url = `https://wa.me/?text=${encodeURIComponent(message)}`;
      window.open(url, '_blank');
    }
  </script>
</body>
</html>
