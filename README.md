<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Best Friend 🎉</title>

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }

    .container {
      padding: 40px;
    }

    h1 {
      font-size: 3rem;
      text-shadow: 2px 2px 10px #ff6f91;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px #ff6f91; }
      to { text-shadow: 0 0 25px #ff3f6c; }
    }

    .sayri {
      font-size: 1.3rem;
      margin: 20px auto;
      max-width: 700px;
      background: rgba(255, 255, 255, 0.2);
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 0 15px rgba(255, 255, 255, 0.3);
    }

    .button {
      background-color: #ff5f7e;
      border: none;
      padding: 15px 30px;
      border-radius: 30px;
      color: white;
      font-size: 1.2rem;
      cursor: pointer;
      transition: 0.3s;
      margin-top: 20px;
    }

    .button:hover {
      background-color: #ff3366;
      transform: scale(1.1);
    }

    .photos {
      display: none;
      margin-top: 30px;
    }

    .photo-box {
      display: inline-block;
      margin: 15px;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
      transition: transform 0.4s;
    }

    .photo-box:hover {
      transform: scale(1.05);
    }

    .photo-box img {
      width: 250px;
      height: 250px;
      object-fit: cover;
    }

    .caption {
      background-color: rgba(255, 255, 255, 0.8);
      color: #ff3366;
      padding: 10px;
      font-weight: bold;
    }

    .bg-photo {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: -1;
      opacity: 0.15;
      background-size: cover;
      background-position: center;
      filter: blur(5px);
    }
  </style>
</head>

<body>
  <div class="bg-photo" style="background-image: url('bgphoto.jpg');"></div>

  <div class="container">
    <h1>🎉 Happy Birthday My Lovely Best Friend 🎂</h1>

    <div class="sayri">
      <p>
        💖 Tere chehre pe hamesha muskaan rahe,<br>
        Zindagi mein hamesha khushiyan rahe,<br>
        Har gham tujhe choo bhi na paaye,<br>
        Tera janmdin har din se khaas ban jaaye! 🎂🌸
      </p>
    </div>

    <button class="button" onclick="showPhotos()">Open Beautiful Memories 💕</button>

    <div class="photos" id="photos">
      <div class="photo-box">
        <img src="photo1.jpg" alt="Best Friend 1">
        <div class="caption">Your smile makes the world brighter 🌷</div>
      </div>
      <div class="photo-box">
        <img src="photo2.jpg" alt="Best Friend 2">
        <div class="caption">Beautiful moments with you 💫</div>
      </div>
      <div class="photo-box">
        <img src="" alt="Best Friend 3">
        <img src="photo3.jpg.jpg" alt="Best Friend 3">
        <div class="caption">Forever my favorite person 💞</div>
      </div>
      <div class="photo-box">
        <img src="photo4.jpg" alt="Best Friend 4">
        <div class="caption">You are a blessing in my life 🎀</div>
      </div>
      <div class="photo-box">
        <img src="photo5.jpg" alt="Best Friend 5">
        <div class="caption">Happy Birthday once again! 🎉</div>
      </div>
    </div>
  </div>

  <script>
    function showPhotos() {
      document.getElementById("photos").style.display = "block";
      window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
    }
  </script>
</body>
</html>
