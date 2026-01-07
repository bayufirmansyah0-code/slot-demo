index.html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<title>Slot Demo</title>
<style>
body{
  background:#0b0b0b;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
  font-family:Arial;
}
.box{
  background:#111;
  padding:30px;
  border-radius:15px;
  text-align:center;
  box-shadow:0 0 20px gold;
}
h1{color:gold;}
.reels{
  display:flex;
  font-size:60px;
  margin:20px 0;
}
.reel{
  width:80px;
  margin:0 10px;
  animation:spin .2s linear infinite;
}
button{
  padding:12px 35px;
  font-size:18px;
  background:gold;
  border:none;
  border-radius:8px;
  cursor:pointer;
}
@keyframes spin{
  0%{transform:translateY(0);}
  100%{transform:translateY(-10px);}
}
</style>
</head>

<body>
<div class="box">
<h1>SLOT DEMO</h1>
<div class="reels">
  <div class="reel" id="r1">🍒</div>
  <div class="reel" id="r2">🍋</div>
  <div class="reel" id="r3">💎</div>
</div>
<button onclick="spin()">SPIN</button>
</div>

<script>
const icons=["🍒","🍋","🔔","💎","⭐"];
function spin(){
  for(let i=1;i<=3;i++){
    document.getElementById("r"+i).innerText =
    icons[Math.floor(Math.random()*icons.length)];
  }
}
</script>
</body>
</html>