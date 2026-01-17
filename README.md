
<!DOCTYPE html>
<html>
<head>
    <title>Small Game</title>
</head>
<body style="text-align:center; font-family:Arial;">

    <h2>🎮 Number Guessing Game</h2>
    <p>Guess a number between 1 and 10</p>

    <input type="number" id="guess" min="1" max="10">
    <br><br>

    <button onclick="checkGuess()">Check</button>

    <p id="result"></p>

    <script>
        let randomNumber = Math.floor(Math.random() * 10) + 1;

        function checkGuess() {
            let userGuess = document.getElementById("guess").value;

            if (userGuess == randomNumber) {
                document.getElementById("result").innerHTML = "🎉 Correct! You won!";
            } else if (userGuess > randomNumber) {
                document.getElementById("result").innerHTML = "📈 Too High!";
            } else {
                document.getElementById("result").innerHTML = "📉 Too Low!";
            }
        }
    </script>

</body>
</html>
