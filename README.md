<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For My Love ❤️</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Segoe UI',sans-serif;}
body{overflow:hidden;}
section{
    height:100vh;
    display:none;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:30px;
}
.active{display:flex;}

.btn{
    padding:14px 35px;
    border:none;
    border-radius:30px;
    font-size:18px;
    cursor:pointer;
    background:white;
    color:#ff2f6e;
    margin-top:15px;
}
.btn:hover{transform:scale(1.1);}

.option{
    padding:15px 40px;
    font-size:20px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:15px;
}
.yes{background:#ff2f6e;color:white;}
.no{background:#444;color:white;position:absolute;}

#p4{position:relative;}

.heart{
    position:fixed;
    top:-10px;
    color:#dd21ba;
    animation:fall linear infinite;
    pointer-events:none;
    z-index:999;
}
@keyframes fall{
    to{transform:translateY(110vh);}
}

#p1{background:linear-gradient(135deg,#f083c6,#bf0050);color:rgba(176, 66, 132, 0.807);}
#p2{background:linear-gradient(135deg,#667eea,#da5252);color:white;flex-direction:column;}
#p3{background:linear-gradient(135deg,#ff9a9e,#fad0c4);color:#4a0033;flex-direction:column;}
#p4{background:linear-gradient(135deg,#ffecd2,#fcb69f);flex-direction:column;}
#p5{background:rgba(165, 8, 8, 0.916);color:#00ff99;flex-direction:column;}

.card{
    background:rgba(255,255,255,0.15);
    padding:40px;
    border-radius:20px;
    animation:float 3s infinite;
}
@keyframes float{
    0%,100%{transform:translateY(0);}
    50%{transform:translateY(-15px);}
}

.gallery{
    display:grid;
    grid-template-columns:repeat(5, 1fr);
    gap:12px;
    margin:20px 0;
}
.gallery img{
    width:120px;
    height:160px;
    border-radius:15px;
    object-fit:cover;
}

img.single{
    width:220px;
    border-radius:20px;
    margin:20px 0;
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<section id="p1" class="active">
<div class="card">
<h1>🎉 Happy Birthday My Love ❤️</h1>
<p>Tum meri zindagi ki sabse khoobsurat wajah ho 💖</p>
<audio id="song1" src="song1.mp3.mp3"></audio>
<button class="btn" onclick="toggle('song1')">🎶 Play Song</button><br>
<button class="btn" onclick="next(1)">Next 💫</button>
</div>
</section>

<!-- PAGE 2 -->
<section id="p2">
<h1>💖 Madam jii 💖</h1>
<div class="gallery">
<img src="photo1.jpg.jpeg">
<img src="photo2.jpg.jpeg">
<img src="photo3.jpg.jpeg">
<img src="photo4.jpg.jpeg">
<img src="photo5.jpg.jpeg">
</div>
<audio id="song2" src="song2.mp3.mp3"></audio>
<button class="btn" onclick="toggle('song2')">🎵 Play Song</button><br>
<button class="btn" onclick="next(2)">Next ❤️</button>
</section>

<!-- PAGE 3 (10 PHOTOS) -->
<section id="p3">
<h1>💌 Our Beautiful Moments 💌</h1>

<div class="gallery">
<img src="p3_1.jpg.jpeg">
<img src="p3_2.jpg.jpeg">
<img src="p3_3.jpg.jpeg">
<img src="p3_4.jpg.jpeg">
<img src="p3_5.jpg.jpeg">
<img src="p3_6.jpg.jpeg">
<img src="p3_7.jpg.jpeg">
<img src="p3_8.jpg.jpeg">
<img src="p3_9.jpg.jpeg">
<img src="p3_10.jpg.jpeg">
</div>

<audio id="song3" src="song3.mp3.mp3"></audio>
<button class="btn" onclick="toggle('song3')">🎶 Play Song</button><br>
<button class="btn" onclick="next(3)">Next 💍</button>
</section>

<!-- PAGE 4 -->
<section id="p4">
<img src="p4.jpg.jpeg" class="single">
<h1>💍 Will You be my madam jii❤️? 💍</h1>
<audio id="song4" src="song4.mp3.mp3"></audio>
<button class="btn" onclick="toggle('song4')">🎶 Play Song</button><br>
<button class="option yes" onclick="saveAnswer('YES ❤️')">YES</button>
<button class="option no" id="noBtn">NO</button>
</section>

<!-- PAGE 5 -->
<section id="p5">
<img src="p5.jpg.jpeg" class="single">
<h1>❤️ Love You meri pyari gudiya ❤️</h1>
<audio id="song5" src="song5.mp3.mp3"></audio>
<button class="btn" onclick="toggle('song5')">🎶 Play Song</button><br>
</section>

<script>
function stopAllSongs(){
    document.querySelectorAll("audio").forEach(a=>{
        a.pause();
        a.currentTime = 0;
    });
}

function next(n){
    stopAllSongs();
    document.getElementById("p"+n).classList.remove("active");
    document.getElementById("p"+(n+1)).classList.add("active");
}

function toggle(id){
    stopAllSongs();
    document.getElementById(id).play();
}

function saveAnswer(ans){
    localStorage.setItem("answer",ans);
    stopAllSongs();
    document.querySelectorAll("section").forEach(s=>s.classList.remove("active"));
    document.getElementById("p5").classList.add("active");
}

document.getElementById("noBtn").onmouseover=function(){
    this.style.left=Math.random()*80+"%";
    this.style.top=Math.random()*80+"%";
};

setInterval(()=>{
    let h=document.createElement("div");
    h.className="heart";
    h.innerHTML="❤️";
    h.style.left=Math.random()*100+"vw";
    h.style.animationDuration=(Math.random()*3+2)+"s";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),5000);
},300);
</script>

</body>
</html>

