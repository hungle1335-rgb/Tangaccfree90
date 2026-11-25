
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nhập Key Để Nhận ACC LQ Free Nha Ae</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #080811;
    color: white;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
    overflow: hidden;
}

/* Background */
body::before {
    content: "";
    position: fixed;
    width: 400px;
    height: 400px;
    background: #7c3aed;
    filter: blur(150px);
    opacity: 0.25;
    top: -100px;
    left: -100px;
}

body::after {
    content: "";
    position: fixed;
    width: 350px;
    height: 350px;
    background: #06b6d4;
    filter: blur(150px);
    opacity: 0.2;
    bottom: -100px;
    right: -100px;
}

.container {
    position: relative;
    z-index: 1;
    width: 100%;
    max-width: 420px;
    padding: 35px 25px;
    background: rgba(18, 18, 32, 0.9);
    border: 1px solid rgba(139, 92, 246, 0.4);
    border-radius: 22px;
    text-align: center;
    box-shadow: 0 0 40px rgba(124, 58, 237, 0.15);
    backdrop-filter: blur(15px);
}

.logo {
    font-size: 55px;
    margin-bottom: 15px;
    filter: drop-shadow(0 0 15px #a855f7);
}

h1 {
    font-size: 25px;
    font-weight: 800;
    line-height: 1.5;
    margin-bottom: 10px;
    background: linear-gradient(90deg, #c084fc, #22d3ee);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.subtitle {
    color: #a1a1aa;
    font-size: 14px;
    margin-bottom: 28px;
    line-height: 1.6;
}

.input-box {
    position: relative;
    margin-bottom: 15px;
}

input {
    width: 100%;
    padding: 16px;
    border-radius: 12px;
    outline: none;
    border: 1px solid #37304f;
    background: #10101c;
    color: white;
    font-size: 15px;
    text-align: center;
    transition: 0.3s;
}

input:focus {
    border-color: #a855f7;
    box-shadow: 0 0 15px rgba(168, 85, 247, 0.2);
}

input::placeholder {
    color: #71717a;
}

button {
    width: 100%;
    padding: 15px;
    border: none;
    border-radius: 12px;
    background: linear-gradient(90deg, #7c3aed, #9333ea, #06b6d4);
    color: white;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 25px rgba(168, 85, 247, 0.4);
}

button:active {
    transform: scale(0.97);
}

#message {
    margin-top: 18px;
    font-size: 14px;
    min-height: 20px;
    line-height: 1.6;
}

.info {
    margin-top: 25px;
    padding-top: 18px;
    border-top: 1px solid #272738;
    font-size: 12px;
    color: #71717a;
    line-height: 1.7;
}

.footer {
    margin-top: 15px;
    color: #52525b;
    font-size: 11px;
}

@media (max-width: 480px) {
    .container {
        padding: 30px 20px;
    }

    h1 {
        font-size: 23px;
    }
}
</style>
</head>

<body>

<div class="container">

    <div class="logo">🎮</div>

    <h1>Nhập Key Để Nhận ACC LQ Free Nha Ae</h1>

    <p class="subtitle">
        Nhập mã Key của bạn để xác nhận chương trình
    </p>

    <div class="input-box">
        <input
            type="text"
            id="keyInput"
            placeholder="Nhập Key tại đây..."
            autocomplete="off"
        >
    </div>

    <button onclick="checkKey()">
        🔓 XÁC NHẬN KEY
    </button>

    <div id="message"></div>

    <div class="info">
        ✨ Giao diện nhận Key phiên bản mới<br>
        🎮 Chúc ae may mắn nha!
    </div>

    <div class="footer">
        © 2026 • LQ FREE ACC
    </div>

</div>

<script>
function checkKey() {
    const key = document.getElementById("keyInput").value.trim();
    const message = document.getElementById("message");

    if (key === "") {
        message.style.color = "#f87171";
        message.innerHTML = "⚠️ Vui lòng nhập Key!";
        return;
    }

    message.style.color = "#fbbf24";
    message.innerHTML = "⏳ Đang kiểm tra Key...";

    setTimeout(() => {
        message.style.color = "#fb7185";
        message.innerHTML =
            "❌ Key chưa được xác thực! Vui lòng kiểm tra lại.";
    }, 1000);
}
</script>

</body>
</html>
