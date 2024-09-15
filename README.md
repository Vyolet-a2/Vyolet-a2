<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Web</title>
    <!-- Include Google Font -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap">
    <style>
        body {
            font-family: 'Patrick Hand', cursive;
            background-color: #FFFAE3;
            color: #333;
            text-align: center;
            padding: 20pixel;
        }

        h1 {
            font-size: 3em;
            color: #FF6F61;
        }

        p {
            font-size: 1.5em;
            color: #4D4D4D;
        }

        .container {
            margin-top: 50px;
            padding: 20px;
            border-radius: 12px;
            background-color: #FDF5E6;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        button {
            padding: 15px 25px;
            margin: 10px 30px;
            font-size: 18px;
            background-color: #FFB6C1;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }

        button:hover {
            transform: scale(1.1);
            background-color: #FF69B4;
        }

        .hidden {
            display: none;
        }

        #options button {
            margin: 20px;
        }

        #response p {
            font-size: 1.8em;
            color: #FF4500;
            transition: opacity 0.6s ease;
            opacity: 0;
        }

        #response.show p {
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hello!! 🌞</h1>
        <p>Thx for reading this web hehehe</p>
        <button onclick="nextPage('page1')">you're welcome</button>
    </div>

    <!-- Page 1: Ask for feeling -->
    <div id="page1" class="container hidden">
        <p>How's your day??</p>
        <button onclick="nextPage('goodPage')">good!</button>
        <button onclick="nextPage('badPage')">not good</button>
    </div>

    <!-- Good response page -->
    <div id="goodPage" class="container hidden">
        <p>Ahaha, glad to hear that! Have a nice day 😊</p>
        <button onclick="nextPage('finalPage')">Next</button>
    </div>

    <!-- Bad response page -->
    <div id="badPage" class="container hidden">
        <p>Ohh, sorry to hear that. Can I help you, babe? 🥺</p>
    </div>

    <!-- Final Page -->
    <div id="finalPage" class="container hidden">
        <p>Thanks for interacting! Hope you enjoy the rest of your day 🌟</p>
    </div>

    <script>
        function nextPage(pageId) {
            // Hide all containers first
            var containers = document.getElementsByClassName('container');
            for (var i = 0; i < containers.length; i++) {
                containers[i].classList.add('hidden');
            }

            // Show the selected page
            document.getElementById(pageId).classList.remove('hidden');
        }
    </script>
</body>
</html>
