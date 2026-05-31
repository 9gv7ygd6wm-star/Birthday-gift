<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Gift</title>

<style>
body{
margin:0;
font-family:Arial,sans-serif;
background:linear-gradient(to bottom,#000,#001f4d);
color:white;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
text-align:center;
}

.page{
display:none;
padding:20px;
}

.active{
display:block;
}

.envelope{
font-size:120px;
cursor:pointer;
}

.candle{
font-size:120px;
cursor:pointer;
}

.cake{
font-size:150px;
}

button{
background:#0066ff;
color:white;
border:none;
padding:12px 25px;
border-radius:10px;
margin-top:20px;
font-size:18px;
cursor:pointer;
}

.message{
font-size:24px;
line-height:1.6;
max-width:600px;
margin:auto;
}
</style>
</head>
<body>

<!-- PAGE 1 -->
<div class="page active" id="page1">
<h1>Tap the Envelope</h1>
<div class="envelope" onclick="showPage(2)">📩</div>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
<h1>Blow the Candle</h1>
<div class="candle" onclick="blowCandle()" id="candle">🕯️</div>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3">
<h1>Happy Birthday!</h1>
<div class="cake">🎂</div>
<button onclick="showPage(4)">Next</button>
</div>

<!-- PAGE 4 -->
<div class="page" id="page4">
<h1>Tap the Envelope Again</h1>
<div class="envelope" onclick="showPage(5)">📩</div>
</div>

<!-- PAGE 5 -->
<div class="page" id="page5">
<h1>Special Message</h1>

<div class="message">
Happy Birthday! 🎉<br><br>

Thank you for being part of my life.
I hope all your dreams come true and that
this year brings you happiness, success,
and countless beautiful memories.

Enjoy your special day. 💙
</div>

<button onclick="showPage(6)">Next</button>
</div>

<!-- PAGE 6 -->
<div class="page" id="page6">
<h1>Dedicated Song 🎵</h1>

<audio controls autoplay>
<source src="song.mp3" type="audio/mpeg">
</audio>

<p>
Replace <b>song.mp3</b> with your dedicated song.
</p>
</div>

<script>
function showPage(num){
document.querySelectorAll('.page').forEach(p=>{
p.classList.remove('active');
});
document.getElementById('page'+num).classList.add('active');
}

function blowCandle(){
document.getElementById("candle").innerHTML="🕯";
setTimeout(()=>{
showPage(3);
},1000);
}
</script>

</body>
</html>
``
