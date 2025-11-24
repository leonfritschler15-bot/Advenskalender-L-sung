<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Adventsrätsel – Lösung</title>
<style>
body {
font-family: Arial, sans-serif;
background: linear-gradient(#c62828, #8e0000);
margin: 0;
padding: 2rem;
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
color: white;
}
.container {
background: white;
padding: 2rem;
border-radius: 12px;
box-shadow: 0 4px 10px rgba(0,0,0,0.1);
max-width: 400px;
width: 100%;
text-align: center;
}
input {
width: 100%;
padding: 0.7rem;
margin-top: 1rem;
border: 1px solid #ccc;
border-radius: 8px;
font-size: 1rem;
}
button {
margin-top: 1rem;
padding: 0.7rem 1.2rem;
font-size: 1rem;
border: none;
background: #0077ff;
color: white;
border-radius: 8px;
cursor: pointer;
}
button:hover {
background: #005fcc;
}
.result {
margin-top: 1rem;
font-weight: bold;
}
#adminPanel {
margin-top: 2rem;
padding-top: 1rem;
border-top: 1px solid #ddd;
display: none;
text-align: left;
}
</style>
</head>
<body>
<div class="container">
<h2>Wer ist die gesuchte Person?</h2>
<p>Gib deinen Tipp ein:</p>
<input id="userFirst" type="text" placeholder="Vorname..." />
<input id="userLast" type="text" placeholder="Nachname..." />
<input id="guessInput" type="text" placeholder="Name der gesuchten Person..." />
<button onclick="checkGuess()">Überprüfen</button>
<div class="result" id="result"></div>


<!-- Admin Login -->
<div style="margin-top:2rem;">
<input id="adminPass" type="password" placeholder="Admin Passwort" />
<button onclick="adminLogin()">Login</button>
</div>


<!-- Admin Panel -->
<div id="adminPanel">
<h3>Admin-Bereich</h3>
<button onclick="exitAdmin()">← Zurück</button>
<p><strong>Alle eingegebenen Antworten:</strong></p>
<ul id="guessList"></ul>
</div>
</div>


<script>
const correctAnswer = "Marcel HHU1";
const adminPassword = "HHU1_27";


function saveGuess(first, last, guess, correct) {
const entry = { first, last, guess, correct, time: new Date().toLocaleString() };
const data = JSON.parse(localStorage.getItem("guesses") || "[]");
</html>
