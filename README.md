<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Player</title>
    <style>
        
        body {
            font-family: Arial, sans-serif;
            background: #f0f0f0;
            text-align: center;
            padding: 50px;
        }

        .player {
            background: #fff;
            padding: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            display: inline-block;
            border-radius: 10px;
        }

        .player h2 {
            font-size: 24px;
            margin-bottom: 10px;
        }

        .controls {
            margin-top: 20px;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            margin: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        audio {
            margin-top: 20px;
            width: 100%;
            outline: none;
        }
    </style>
</head>
<body>

    <div class="player">
        <h2> Music Player</h2>

        
        <audio id="audioPlayer" controls>
            <source src="song.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>

        <div class="controls">
            <button onclick="playMusic()">Play</button>
            <button onclick="pauseMusic()">Pause</button>
            <button onclick="stopMusic()">Stop</button>
        </div>
    </div>

    <script>
       
        var audio = document.getElementById('audioPlayer');

        
        function playMusic() {
            audio.play();
        }

        
        function pauseMusic() {
            audio.pause();
        }

        
        function stopMusic() {
            audio.pause();
            audio.currentTime = 0; 
        }
    </script>

</body>
</html>
