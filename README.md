<!DOCTYPE html>
## To my Girlfriend Kai Yi
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do you want to be my VALENTINE BB?</title>
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
        <h2 id="question">Do you want to be my VALENTINE BB??</h2>

        <!-- Yes Button -->
        <button class="btn" onclick="answer('YESSS OFC')">Yes</button>

        <!-- No Button -->
        <button class="btn" onclick="answer('NO,FUCK YOU BITCH')">No</button>
    </div>

    <script>
        // Function to handle the user's answer
        function answer(response) {
            // Access the question container and update it dynamically
            const questionContainer = document.getElementById("question-container");

            // If they answered "Yes"
            if (response === 'YESSS OFC') {
                questionContainer.innerHTML = `
                    <h2>!YAY!</h2>
                    <p>I LOVE YOU!</p>
                `;
            } 
            // If they answered "No", ask if they like tea
            else if (response === 'NO,FUCK YOU BITCH') {
                questionContainer.innerHTML = `
                    <h2>PLEASEEEE BE MY VALENTINE</h2>
                    <button class="btn" onclick="answerTea('FINE,ONLY CAUSE U CUTE')">Yes</button>
                    <button class="btn" onclick="answerTea('I SAID NO ALREADY U BITCH')">No</button>
                `;
            }
        }

        // Function to handle the "PLEASEEEE BE MY VALENTINE" question
        function answerTea(response) {
            const questionContainer = document.getElementById("question-container");

            if (response === 'FINE,ONLY CAUSE U CUTE') {
                questionContainer.innerHTML = `
                    <h2>YAY!</h2>
                    <p>I KNEW YOU LOVED ME!</p>
                `;
            } else {
                questionContainer.innerHTML = `
                    <h2>GO FUCK YOURSELF BITCH</h2>
                `;
            }
        }
    </script>

</body>
</html>
