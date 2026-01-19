# TT-PANEL
Tiktok like and view bot which help you to increase views on your account 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TikTok Growth Panel</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: radial-gradient(circle at top, #0f172a, #020617);
    color: white;
}

.navbar {
    display: flex;
    justify-content: space-between;
    padding: 20px 40px;
    background: rgba(15, 23, 42, 0.9);
    box-shadow: 0 0 10px rgba(34, 211, 238, 0.3);
}

.logo {
    font-size: 22px;
    font-weight: 600;
    color: #22d3ee;
}

.container {
    max-width: 600px;
    margin: 60px auto;
    background: linear-gradient(145deg, #0b1220, #111827);
    padding: 25px;
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(34, 211, 238, 0.2);
    text-align: center;
    animation: fadeIn 1s ease-in-out;
}

h2 {
    color: #22d3ee;
}

.input-box {
    width: 95%;
    padding: 12px;
    border-radius: 8px;
    border: none;
    outline: none;
    background: #020617;
    color: white;
    margin-top: 10px;
}

select {
    width: 100%;
    padding: 12px;
    border-radius: 8px;
    margin-top: 10px;
    background: #020617;
    color: white;
    border: none;
}

button {
    margin-top: 15px;
    width: 100%;
    padding: 12px;
    border-radius: 8px;
    background: linear-gradient(90deg, #22d3ee, #0ea5e9);
    color: #020617;
    font-weight: bold;
    border: none;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    transform: scale(1.03);
    box-shadow: 0 0 10px #22d3ee;
}

.status {
    margin-top: 15px;
    font-size: 14px;
    color: #86efac;
}

.features {
    display: flex;
    justify-content: space-around;
    margin-top: 30px;
}

.card {
    background: #020617;
    padding: 15px;
    border-radius: 10px;
    width: 28%;
    text-align: center;
    box-shadow: 0 0 10px rgba(34, 211, 238, 0.2);
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}
</style>
</head>

<body>

<div class="navbar">
    <div class="logo">TikTok Booster</div>
    <div>Dashboard</div>
</div>

<div class="container">
    <h2>🚀 TikTok Growth Panel</h2>
    <p>Paste your TikTok video link below:</p>

    <input class="input-box" id="link" type="text" placeholder="Paste TikTok link here">

    <select id="option">
        <option value="views">Increase Views</option>
        <option value="likes">Increase Likes</option>
        <option value="shares">Increase Shares</option>
    </select>

    <button onclick="startProcess()">Start Boost</button>

    <p class="status" id="status"></p>

    <div class="features">
        <div class="card">⚡ Fast Delivery</div>
        <div class="card">🔒 Secure System</div>
        <div class="card">📊 Real-Time Stats</div>
    </div>
</div>

<script>
function startProcess() {
    let link = document.getElementById("link").value;
    let option = document.getElementById("option").value;
    let status = document.getElementById("status");

    if (link === "") {
        status.innerHTML = "⚠️ Please enter a valid TikTok link!";
        status.style.color = "red";
        return;
    }

    status.innerHTML = "⏳ Processing " + option + " for your video...";
    
    setTimeout(() => {
        status.innerHTML = "✅ Task completed successfully! (Demo Mode)";
    }, 3000);
}
</script>

</body>
</html>
