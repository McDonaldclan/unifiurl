<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment Received</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f5f5f7;
        }
        .card {
            background: #ffffff;
            padding: 40px 30px;
            border-radius: 18px;
            box-shadow: 0 4px 14px rgba(0,0,0,0.1);
            text-align: center;
            max-width: 400px;
        }
        .checkmark {
            font-size: 48px;
            margin-bottom: 10px;
        }
        h1 {
            color: #1d1d1f;
            font-size: 24px;
            margin: 0 0 10px 0;
        }
        p {
            color: #86868b;
            font-size: 16px;
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="checkmark">✅</div>
        <h1>Your payment of $200 has been received.</h1>
        <p>You are now connected to the WiFi.</p>
    </div>

    <script>
        // URL for the Apple Pay success chime
        const successSound = new Audio('https://www.myinstants.com/media/sounds/apple-pay-success-sound-effect.mp3');
        
        // Attempt to play the sound as soon as the page loads
        window.onload = () => {
            successSound.play().catch(error => {
                console.log("Browser autoplay policy prevented the sound from playing automatically.");
            });
        };
    </script>
</body>
</html>
