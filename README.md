<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Guess the Number Game</title>
</head>
<body>
  <h1>Guess the Number Game</h1>
  <p>Guess a number between 1 and 10:</p>
  <input type="number" id="guessField">
  <button onclick="checkGuess()">Submit Guess</button>
  <p id="message"></p>

  <script>
    function checkGuess() {
      const randomNumber = Math.floor(Math.random() * 10) + 1;
      const guess = parseInt(document.getElementById('guessField').value);

      if (isNaN(guess) || guess < 1 || guess > 10) {
        document.getElementById('message').innerHTML = 'Please enter a valid number between 1 and 10.';
        return;
      }

      if (guess === randomNumber) {
        document.getElementById('message').innerHTML = `Congratulations! You guessed the correct number (${randomNumber}).`;
      } else {
        document.getElementById('message').innerHTML = `Sorry, the correct number was ${randomNumber}. Try again!`;
      }
    }
  </script>
</body>
</html>

