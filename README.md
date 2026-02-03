# Valentine-for-viruuuu-
<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <title>Viruuu 💕</title>  
  <style>  
    body {  
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);  
      font-family: 'Comic Sans MS', cursive;  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      text-align: center;  
      margin: 0;  
    }  
  
    .card {  
      background: white;  
      padding: 40px;  
      border-radius: 20px;  
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);  
      width: 320px;  
    }  
  
    h1 {  
      color: #ff4d6d;  
    }  
  
    button {  
      padding: 12px 20px;  
      font-size: 16px;  
      border: none;  
      border-radius: 12px;  
      cursor: pointer;  
      margin: 10px;  
      transition: 0.3s;  
    }  
  
    #yesBtn {  
      background: #ff4d6d;  
      color: white;  
    }  
  
    #noBtn {  
      background: #ccc;  
    }  
  
    .hearts {  
      font-size: 30px;  
      animation: float 1s infinite alternate;  
    }  
  
    @keyframes float {  
      from { transform: translateY(0); }  
      to { transform: translateY(-10px); }  
    }  
  </style>  
</head>  
<body>  
  
  <div class="card">  
    <h1>Viruuu 💕</h1>  
    <p id="question">Will you be my Valentine? 🥺💘</p>  
  
    <button id="yesBtn" onclick="yesClicked()">YES 💖</button>  
    <button id="noBtn" onclick="noClicked()">NO 🙃</button>  
  </div>  
  
  <script>  
    let noCount = 0;  
  
    const noTexts = [  
      "Are you sure? 🥺",  
      "Really really sure? 😭",  
      "But I love you 🥹💕",  
      "Viruuu pleaseee 😔",  
      "Think again 😠❤️",  
      "I will cry now 😢",  
      "My heart is breaking 💔",  
      "Last chance 😤💕",  
      "Okay but I’m still yours 😌"  
    ];  
  
    function noClicked() {  
      const text = document.getElementById("question");  
      const yesBtn = document.getElementById("yesBtn");  
  
      text.innerText = noTexts[noCount % noTexts.length];  
      noCount++;  
  
      // Make YES button bigger every time  
      let size = 16 + noCount * 4;  
      yesBtn.style.fontSize = size + "px";  
      yesBtn.style.padding = (12 + noCount * 2) + "px";  
    }  
  
    function yesClicked() {  
      document.body.innerHTML = `  
        <div class="card">  
          <h1>YAYYYYY 💕💖</h1>  
          <p>You’re officially my Valentine, Viruuu 😍</p>  
          <div class="hearts">💖💘💕💞💓</div>  
          <p>I love you soooo much 😘</p>  
        </div>  
      `;  
    }  
  </script>  
  
</body>  
</html>  
