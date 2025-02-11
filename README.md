# tt
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yes or No Question</title>
    <style>
        /* Set the background color to light pink */
        body {
            background-color: #f8d0d6;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        /* Style the container for the question and buttons */
        .container {
            text-align: center;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        /* Style the buttons */
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

        /* Hover effect for buttons */
        .btn:hover {
            background-color: #ff5f78;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Display the Yes or No Question -->
        <h2>Do you prefer using self-check-in kiosks over traditional check-in counters when traveling?</h2>
        
        <!-- Yes Button -->
        <button class="btn" onclick="answer('yes')">Yes</button>
        
        <!-- No Button -->
        <button class="btn" onclick="answer('no')">No</button>
    </div>

    <script>
        // This function handles the button clicks
        function answer(response) {
            // Depending on the answer, redirect to a different page with another question
            if(response === 'yes') {
                window.location.href = "page2_yes.html"; // Redirects to another page with a new question for 'Yes' answer
            } else {
                window.location.href = "page2_no.html"; // Redirects to another page with a new question for 'No' answer
            }
        }
    </script>
</body>
</html>
