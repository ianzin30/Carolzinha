# Carolzinha

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Romantic Video Page</title>
    <!-- Include the custom font -->
    <link href="https://fonts.googleapis.com/css?family=Great+Vibes&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Background Video Container -->
    <div class="video-container">
        <video id="background-video" autoplay muted loop playsinline>
            <source src="your-video.mp4" type="video/mp4">
            Your browser does not support HTML5 video.
        </video>
        <!-- Subtitle Text -->
        <div class="subtitle">
            <h2>Your Subtitle Text Here</h2>
        </div>
    </div>

    <!-- Forward Button -->
    <a href="page2.html" class="forward-button">
        <img src="forward-button.png" alt="Next">
    </a>

    <!-- Background Music -->
    <audio id="background-music" loop>
        <source src="your-music.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <!-- JavaScript to synchronize video and audio -->
    <script>
        // Get video and audio elements
        const video = document.getElementById('background-video');
        const audio = document.getElementById('background-music');

        // Play audio when video starts
        video.addEventListener('play', () => {
            audio.currentTime = video.currentTime;
            audio.play();
        });

        // Pause audio when video pauses
        video.addEventListener('pause', () => {
            audio.pause();
        });

        // Sync audio when video loops
        video.addEventListener('ended', () => {
            audio.currentTime = 0;
        });

        // Update audio time when video seeks
        video.addEventListener('timeupdate', () => {
            if (Math.abs(video.currentTime - audio.currentTime) > 0.5) {
                audio.currentTime = video.currentTime;
            }
        });
    </script>

</body>
</html>

Nos conhecemos em um lugar onde eu tinha quase total certeza de que eu nem iria, eu cheguei de viagem exatamente um dia antes da festa em que nos conhecemos, na verdade eu nem era muito fã de festas até te conhecer, sua energia corresponde a pessoa mais alegre que já conheci</h2>
        </div>