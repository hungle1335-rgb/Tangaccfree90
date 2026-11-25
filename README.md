
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LQ FREE ACC - KEY SYSTEM</title>

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
    align-items: center;
    justify-content: center;
    padding: 20px;
}

.container {
    width: 100%;
    max-width: 430px;
    background: #151525;
    border: 1px solid #7137c9;
    border-radius: 20px;
    padding: 30px 23px;
    text-align: center;
    box-shadow: 0 0 30px #7c3aed33;
}

.logo {
    font-size: 55px;
    margin-bottom: 15px;
}

h1 {
    color: #c084fc;
    font-size: 25px;
    margin-bottom: 12px;
}

p {
    color: #aaa;
    font-size: 14px;
    margin-bottom: 22px;
    line-height: 1.6;
}

input {
    width: 100%;
    padding: 15px;
    background: #090914;
    border: 1px solid #51416f;
    border-radius: 10px;
    outline: none;
    color: white;
    text-align: center;
    font-size: 15px;
    margin-bottom: 15px;
}

input:focus {
    border-color: #a855f7;
}

button {
    width: 100%;
    padding: 14px;
    border: none;
    border-radius: 10px;
    background: linear-gradient(90deg,#7c3aed,#a855f7);
    color: white;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    margin-bottom: 12px;
}

button:hover {
    opacity: 0.85;
}

.admin {
    display: none;
}

.key-result {
    background: #090914;
    border: 1px dashed #a855f7;
    border-radius: 10px;
    padding: 18px 10px;
    color: #4ade80;
    font-size: 17px;
    font-weight: bold;
    word-break: break-all;
    margin: 18px 0;
}

.message {
    font-size: 13px;
    min-height: 20px;
    margin-top: 8px;
}

.back {
    background: #29293b;
}

.footer {
    margin-top: 15px;
    color: #666;
    font-size: 11px;
}
</style>
</head>

<body>

<!-- TRANG NHẬP KEY -->
<div class="container" id="login">

    <div class="logo">🎮</div>

    <h1>Nhập Key Để Nhận ACC LQ Free Nha Ae</h1>

    <p>Nhập Key để tiếp tục vào hệ thống</p>

    <input
        type="text"
        id="keyInput"
        placeholder="Nhập Key tại đây..."
    >

    <button onclick="checkKey()">
        🔓 XÁC NHẬN KEY
    </button>

    <div class="message" id="loginMessage"></div>

    <div class="footer">
        © 2026 LQ FREE ACC
    </div>

</div>


<!-- GIAO DIỆN ADMIN -->
<div class="container admin" id="admin">

    <div class="logo">👑</div>

    <h1>ADMIN CONTROL PANEL</h1>

    <p>Chào mừng Admin đến với hệ thống tạo Key!</p>

    <button onclick="generateKey()">
        ✨ TẠO KEY MỚI
    </button>

    <div class="key-result" id="newKey">
        KEY CHƯA ĐƯỢC TẠO
    </div>

    <button onclick="copyKey()">
        📋 SAO CHÉP KEY
    </button>

    <div class="message" id="adminMessage"></div>

    <button class="back" onclick="goBack()">
        ↩ QUAY LẠI
    </button>

    <div class="footer">
        ADMIN SYSTEM • LQ FREE ACC
    </div>

</div>


<script>

// KEY ADMIN
const ADMIN_KEY = "tangaccfree902016";

let currentKey = "";

// KIỂM TRA KEY
function checkKey() {

    const key = document.getElementById("keyInput").value.trim();
    const message = document.getElementById("loginMessage");

    if (key === "") {
        message.style.color = "#f87171";
        message.innerText = "⚠️ Vui lòng nhập Key!";
        return;
    }

    if (key === ADMIN_KEY) {

        document.getElementById("login").style.display = "none";
        document.getElementById("admin").style.display = "block";

    } else {

        message.style.color = "#f87171";
        message.innerText = "❌ Key không chính xác!";

    }
}

// TẠO KEY NGẪU NHIÊN
function generateKey() {

    const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";

    let key = "LQFREE-";

    for (let i = 0; i < 16; i++) {
        key += chars[Math.floor(Math.random() * chars.length)];
    }

    currentKey = key;

    document.getElementById("newKey").innerText = key;

    document.getElementById("adminMessage").style.color = "#4ade80";
    document.getElementById("adminMessage").innerText =
        "✅ Tạo Key thành công!";
}

// SAO CHÉP KEY
function copyKey() {

    if (!currentKey) {
        document.getElementById("adminMessage").innerText =
            "⚠️ Bạn chưa tạo Key!";
        return;
    }

    navigator.clipboard.writeText(currentKey)
    .then(() => {
        document.getElementById("adminMessage").innerText =
            "✅ Đã sao chép Key!";
    })
    .catch(() => {
        document.getElementById("adminMessage").innerText =
            "Không thể sao chép tự động!";
    });
}

// QUAY LẠI
function goBack() {

    document.getElementById("admin").style.display = "none";
    document.getElementById("login").style.display = "block";

    document.getElementById("keyInput").value = "";
    document.getElementById("loginMessage").innerText = "";

}

</script>

</body>
</html>
