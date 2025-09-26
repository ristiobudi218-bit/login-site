# login-site
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Login Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .login-box {
      background: #fff;
      padding: 20px 30px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 300px;
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }
    input {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button {
      width: 100%;
      padding: 10px;
      background: #4285F4;
      color: white;
      border: none;
      border-radius: 4px;
      font-weight: bold;
      cursor: pointer;
    }
    button:hover {
      background: #3367D6;
    }
    .msg {
      text-align: center;
      margin-top: 10px;
      font-size: 14px;
      color: red;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>Login</h2>
    <form onsubmit="return checkLogin()">
      <input type="text" id="username" placeholder="Username" required>
      <input type="password" id="password" placeholder="Password" required>
      <button type="submit">Login</button>
    </form>
    <div class="msg" id="message"></div>
  </div>

  <script>
    function checkLogin() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      const msg = document.getElementById("message");

      // Contoh login sederhana (username & password statis)
      if (user === "admin" && pass === "12345") {
        msg.style.color = "green";
        msg.textContent = "Login berhasil ✅";
        // Redirect ke halaman lain setelah login sukses
        setTimeout(() => {
          window.location.href = "[https://sites.google.com](https://docs.google.com/forms/d/1kimnxz88D-ayXtNi2Y94lIyYzUKtR7kk5AZHrdx-5qU/edit)/"; 
        }, 1500);
      } else {
        msg.textContent = "Username atau password salah ❌";
      }
      return false; // biar form tidak reload
    }
  </script>
</body>
</html>
