# tt
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Like Coffee?</title>
    <style>
        body {
            background-color: #f8d0d6; /* Light pink background */
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        .btn {
            background-color: #ff87a2;
            color: white;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        .btn:hover {
            background-color: #ff5f78;
        }
    </style>
</head>
<body>

    <div class="container" id="question-container">
        <!-- Initial Question -->
        <h2 id="question">Do you like coffee?</h2>

        <!-- Yes Button -->
        <button class="btn" onclick="answer('yes')">Yes</button>

        <!-- No Button -->
        <button class="btn" onclick="answer('no')">No</button>
    </div>

    <script>
        // Function to handle the user's answer
        function answer(response) {
            // Access the question container and update it dynamically
            const questionContainer = document.getElementById("question-container");

            // If they answered "Yes", give a free coffee message
            if (response === 'yes') {
                questionContainer.innerHTML = `
                    <h2>Here is your free coffee! ☕</h2>
                    <p>Enjoy your coffee!</p>
                `;
            } 
            // If they answered "No", ask if they like tea
            else if (response === 'no') {
                questionContainer.innerHTML = `
                    <h2>Do you like tea?</h2>
                    <button class="btn" onclick="answerTea('yes')">Yes</button>
                    <button class="btn" onclick="answerTea('no')">No</button>
                `;
            }
        }

        // Function to handle the "Do you like tea?" question
        function answerTea(response) {
            const questionContainer = document.getElementById("question-container");

            if (response === 'yes') {
                questionContainer.innerHTML = `
                    <h2>Thanks for your response! You like tea!</h2>
                `;
            } else {
                questionContainer.innerHTML = `
                    <h2>Thanks for your response! You don't like tea!</h2>
                `;
            }
        }
    </script>

</body>
</html>
