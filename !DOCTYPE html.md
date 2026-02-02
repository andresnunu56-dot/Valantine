#   
<!DOCTYPE html>  
<html lang="sv">  
<head>  
  <meta charset="UTF-8">  
  <title>Valentine 💘</title>  
  <style>  
    body {  
      margin: 0;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      background: linear-gradient(#ffb6c1, #ff69b4);  
      font-family: Arial, sans-serif;  
      overflow: hidden;  
    }  
  
    .card {  
      background: white;  
      padding: 25px;  
      text-align: center;  
      border-radius: 20px;  
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);  
      width: 300px;  
      position: relative;  
      z-index: 2;  
    }  
  
    img {  
      width: 180px;  
      border-radius: 15px;  
    }  
  
    h2 {  
      margin: 15px 0;  
    }  
  
    .buttons {  
      margin-top: 20px;  
      position: relative;  
      height: 80px;  
    }  
  
    button {  
      padding: 10px 20px;  
      font-size: 16px;  
      border: none;  
      border-radius: 10px;  
      cursor: pointer;  
    }  
  
    #yes {  
      background: #ff4d6d;  
      color: white;  
    }  
  
    #no {  
      background: #ccc;  
      position: absolute;  
    }  
  
    .heart {  
      position: fixed;  
      top: -10px;  
      font-size: 20px;  
      animation: fall linear forwards;  
      color: #ff4d6d;  
      z-index: 1;  
    }  
  
    @keyframes fall {  
      to {  
        transform: translateY(110vh);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
<body>  
  
<div class="card">  
  <img src="https://i.imgur.com/8Km9tLL.png">  
  <h2>Vill du bli min Valentine? 💘</h2>  
  
  <div class="buttons">  
    <button id="yes" onclick="alert('JAG VISSTE DET!! 😍💖')">Ja 💖</button>  
    <button id="no">Nej 😢</button>  
  </div>  
</div>  
  
<script>  
  // Nej-knappen flyr 😏  
  const noBtn = document.getElementById("no");  
  noBtn.addEventListener("mouseover", () => {  
    const x = Math.random() * 200;  
    const y = Math.random() * 50;  
    noBtn.style.left = x + "px";  
    noBtn.style.top = y + "px";  
  });  
  
  // Fallande hjärtan 💕  
  function createHeart() {  
    const heart = document.createElement("div");  
    heart.classList.add("heart");  
    heart.innerText = "💖";  
    heart.style.left = Math.random() * 100 + "vw";  
    heart.style.animationDuration = Math.random() * 3 + 2 + "s";  
    heart.style.fontSize = Math.random() * 20 + 10 + "px";  
    document.body.appendChild(heart);  
  
    setTimeout(() => {  
      heart.remove();  
    }, 5000);  
  }  
  
  setInterval(createHeart, 300);  
</script>  
  
</body>  
</html>  
