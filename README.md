<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MSBD Website</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(135deg, #ffb6c1, #ff69b4);
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .container {
      background: rgba(255, 255, 255, 0.25);
      backdrop-filter: blur(10px);
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      max-width: 600px;
      width: 100%;
      color: #ffffff;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      animation: fadeIn 1.5s ease;
    }

    h1 {
      font-size: 2.8rem;
      margin-bottom: 20px;
    }

    p {
      font-size: 1.2rem;
      line-height: 1.6;
    }

    .btn {
      display: inline-block;
      margin-top: 30px;
      padding: 14px 30px;
      background: #ffffff;
      color: #ff4f9a;
      text-decoration: none;
      font-weight: bold;
      border-radius: 30px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #ff4f9a;
      color: #ffffff;
      transform: scale(1.05);
    }

    footer {
      margin-top: 25px;
      font-size: 0.9rem;
      opacity: 0.9;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2.2rem;
      }
      p {
        font-size: 1.1rem;
      }
    }
  </style>
</head>

<body>

  <div class="container">
    <h1>Happy Birthday 🎉</h1>
    <p>
      Wishing you a day filled with happiness, smiles,  
      and wonderful memories.  
      May this year bring you success and joy.
    </p>

    <a class="btn" href="#">Have a Wonderful Day</a>

    <footer>
      — Made by Vishvraj
    </footer>
  </div>

</body>
</html>