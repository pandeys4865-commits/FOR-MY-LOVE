<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Propose Day</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff4d6d, #ff85a1);
    overflow: hidden;
    font-family: 'Segoe UI', sans-serif;
  }

  .message {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
    z-index: 2;
  }

  .message h1 {
    font-size: 2.5rem;
    margin-bottom: 10px;
  }

  .message .kiss {
    font-size: 4rem;
    margin-top: 10px;
  }

  .heart {
    position: absolute;
    bottom: -20px;
    color: rgba(255, 255, 255, 0.8);
    font-size: 20px;
    animation: floatUp linear infinite;
  }

  @keyframes floatUp {
    from {
      transform: translateY(0);
      opacity: 1;
    }
    to {
      transform: translateY(-110vh);
      opacity: 0;
    }
  }
</style>
</head>
<body>

<div class="message">
  <h1>Happy Propose Day,<br>My Love ❤️</h1>
  <div class="kiss">💋</div>
</div>

<script>
  function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    heart.style.animationDuration = Math.random() * 3 + 3 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 6000);
  }

  setInterval(createHeart, 300);
</script>

</body>
</html>
