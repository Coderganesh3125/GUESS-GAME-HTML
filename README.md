# GUESS-GAME-HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Guess the Number</title>
<style>
body {
	text-align: center;
	font-family: Arial, sans-serif;
}

input {
	width: 100px;
	padding: 5px;
}

button {
	font-size: 18px;
	padding: 5px;
	margin: 5px;
}
</style>
</head>
<body>
	<h1>Guess the Number (1-10)</h1>
	<input type="number" id="guess" placeholder="Enter number">
	<button onclick="checkGuess()">Guess</button>
	<h2 id="message">message will be printed here</h2>
	<script>
		let randomNumber = Math.floor(Math.random() * 10) + 1;
		function checkGuess() {
			console.log(randomNumber);
			randomNumber=7;
			let userGuess = parseInt(document.getElementById("guess").value);
			if (userGuess === randomNumber) {
				document.getElementById("message").textContent = " Correct! You guessed it!";
			} else if (userGuess > randomNumber) {
				document.getElementById("message").textContent = "Too high! Try again.";
			} else {
				document.getElementById("message").textContent = "Too low! Try again.";
			}
		}
	</script>
</body>
</html>
