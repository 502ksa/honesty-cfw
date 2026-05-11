# honesty-cfw

<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;700;900&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
font-family:'Tajawal',sans-serif;
}

body{
background:#050b17;
color:white;
overflow-x:hidden;
}

header{
position:fixed;
top:0;
width:100%;
padding:20px 7%;
display:flex;
justify-content:space-between;
align-items:center;
backdrop-filter:blur(10px);
background:rgba(5,11,23,.7);
z-index:999;
border-bottom:1px solid rgba(255,255,255,.05);
}

.logo{
font-size:32px;
font-weight:900;
color:#4b8cff;
}

nav{
display:flex;
gap:25px;
}

nav a{
color:white;
text-decoration:none;
font-size:17px;
transition:.3s;
}

nav a:hover{
color:#4b8cff;
}

.hero{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:0 20px;
background:
linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
url('https://images.unsplash.com/photo-1511512578047-dfb367046420?q=80&w=2070') center/cover;
}

.hero-content h1{
font-size:75px;
font-weight:900;
margin-bottom:20px;
}

.hero-content p{
font-size:22px;
opacity:.8;
margin-bottom:35px;
}

.btn{
padding:14px 35px;
background:#215cff;
border:none;
border-radius:12px;
color:white;
font-size:18px;
cursor:pointer;
transition:.3s;
}

.btn:hover{
transform:translateY(-4px);
background:#3a72ff;
}

section{
padding:120px 7%;
}

.section-title{
font-size:45px;
margin-bottom:50px;
font-weight:900;
text-align:center;
}

.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
}

.card{
background:rgba(255,255,255,.04);
padding:30px;
border-radius:20px;
border:1px solid rgba(255,255,255,.05);
transition:.3s;
}

.card:hover{
transform:translateY(-7px);
border-color:#215cff;
}

.card h3{
font-size:28px;
margin-bottom:10px;
}

.card p{
opacity:.7;
line-height:1.7;
}

.live-box{
background:linear-gradient(135deg,#163a80,#215cff);
padding:50px;
border-radius:25px;
text-align:center;
}

.live-box h2{
font-size:50px;
margin-bottom:10px;
}

.live-box p{
font-size:22px;
opacity:.9;
}

footer{
padding:30px;
text-align:center;
background:#09111f;
border-top:1px solid rgba(255,255,255,.05);
}

@media(max-width:768px){

.hero-content h1{
font-size:48px;
}

.section-title{
font-size:35px;
}

nav{
display:none;
}

}

</style>
</head>
<body>

<header>

<div class="logo">
Honesty CFW
</div>

<nav>
<a href="#team">الفريق</a>
<a href="#store">المتجر</a>
<a href="#live">البث المباشر</a>
<a href="#creators">صناع المحتوى</a>
</nav>

</header>

<section class="hero">

<div class="hero-content">

<h1>Honesty CFW</h1>

<p>
أفضل سيرفر CFW بإدارة احترافية وتجربة فريدة
</p>

<button class="btn">
دخول السيرفر
</button>

</div>

</section>

<section id="team">

<h2 class="section-title">
الفريق
</h2>

<div class="grid">

<div class="card">
<h3>Owner</h3>
<p>Ahmed</p>
</div>

<div class="card">
<h3>Founders</h3>
<p>Faisal - Talal</p>
</div>

<div class="card">
<h3>High Management</h3>
<p>Management Team</p>
</div>

</div>

</section>

<section id="store">

<h2 class="section-title">
المتجر
</h2>

<div class="grid">

<div class="card">
<h3>VIP Package</h3>
<p>يمكنك تعديل المنتجات وإضافة أي شيء تريده</p>
</div>

<div class="card">
<h3>Mafia Package</h3>
<p>بكجات مخصصة للعصابات والمافيا</p>
</div>

<div class="card">
<h3>Vehicles</h3>
<p>إضافة سيارات وباقات متنوعة</p>
</div>

</div>

</section>

<section id="live">

<div class="live-box">

<h2 id="liveCount">
24
</h2>

<p>
عدد البثوث الحالية
</p>

</div>

</section>

<section id="creators">

<h2 class="section-title">
صناع المحتوى
</h2>

<div class="grid">

<div class="card">
<h3>RV</h3>
<p>Streamer</p>
</div>

<div class="card">
<h3>Darkness</h3>
<p>Content Creator</p>
</div>

<div class="card">
<h3>Honesty Clips</h3>
<p>Media Team</p>
</div>

</div>

</section>

<footer>

Honesty CFW © 2026

</footer>

<script>

const count = document.getElementById("liveCount");

let num = 0;

const target = 24;

const interval = setInterval(()=>{

num++;

count.innerText = num;

if(num >= target){
clearInterval(interval);
}

},50);

</script>

</body>
</html>
