<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800;900&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Tajawal',sans-serif;background:#0a0c14;color:#fff;overflow-x:hidden;}

::-webkit-scrollbar{width:5px;}
::-webkit-scrollbar-track{background:#0a0c14;}
::-webkit-scrollbar-thumb{background:#1e5eff;border-radius:10px;}

/* NAV */
.navbar{
  position:fixed;top:0;left:0;width:100%;z-index:1000;
  display:flex;justify-content:space-between;align-items:center;
  padding:0 40px;height:65px;
  background:rgba(8,10,20,0.85);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(30,94,255,0.15);
}
.nav-logo{font-size:20px;font-weight:900;color:#fff;}
.nav-logo span{color:#1e5eff;}
.nav-links{display:flex;gap:4px;}
.nav-links button{
  background:transparent;border:none;color:rgba(255,255,255,0.75);
  padding:8px 16px;border-radius:8px;cursor:pointer;
}
.nav-links button:hover,.nav-links button.active{
  color:#fff;background:rgba(30,94,255,0.15);
}
.nav-shop{background:#1e5eff!important;color:#fff!important;border-radius:8px;}

/* CONTAINER */
.container{padding-top:65px;}
.page{display:none;}
.active{display:block;}

/* HERO */
.hero{
  position:relative;min-height:100vh;
  display:flex;align-items:center;justify-content:center;text-align:center;
}
.hero-bg{
  position:absolute;inset:0;
  background:url('https://images.unsplash.com/photo-1520975916090-3105956dac38?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
  z-index:-2;
}
.hero-bg::after{
  content:'';position:absolute;inset:0;
  background:rgba(0,0,0,0.6);
}
.hero-content{z-index:2;max-width:700px;}
.hero h1{font-size:60px;font-weight:900;}
.hero h1 span{color:#1e5eff;}
.hero p{opacity:.7;margin:10px 0 20px;}

.btn-primary{
  background:#1e5eff;color:#fff;padding:12px 25px;border:none;border-radius:10px;
}

/* SECTIONS */
.section{padding:80px 40px;max-width:1100px;margin:auto;}
.section-title{font-size:28px;font-weight:900;margin-bottom:20px;}
.section-sub{opacity:.6;margin-bottom:40px;}

.card{
  background:rgba(255,255,255,0.05);
  padding:20px;border-radius:12px;margin:10px 0;
}

/* ADMIN BUTTON */
.admin-btn{
  position:fixed;left:15px;top:15px;z-index:2000;
  background:#ffcc00;color:#000;
  border:none;padding:8px 12px;
  border-radius:8px;font-weight:900;cursor:pointer;
}

/* ADMIN PANEL */
.admin-panel{
  position:fixed;top:80px;left:15px;width:280px;
  background:#111827;border:1px solid #1e5eff;
  padding:15px;border-radius:12px;z-index:3000;
}
.admin-panel button{
  width:100%;margin:5px 0;padding:8px;
  background:#1e5eff;color:#fff;border:none;border-radius:8px;
}
.close-btn{background:red!important;}
</style>
</head>

<body>

<!-- زر المشرف -->
<button class="admin-btn" onclick="adminLogin()">مشرف</button>

<!-- NAV -->
<div class="navbar">
  <div class="nav-logo"><span>Honesty</span> CFW</div>
  <div class="nav-links">
    <button class="active" onclick="show('home',this)">الرئيسية</button>
    <button onclick="show('creators',this)">صناع المحتوى</button>
    <button onclick="show('live',this)">البث</button>
    <button onclick="show('team',this)">الفريق</button>
    <button onclick="show('shop',this)" class="nav-shop">المتجر</button>
    <button onclick="show('rules',this)">القوانين</button>
  </div>
</div>

<div class="container">

<!-- HOME -->
<div id="home" class="page active">
  <div class="hero">
    <div class="hero-bg"></div>
    <div class="hero-content">
      <h1>Honesty <span>CFW</span></h1>
      <p>أقوى سيرفر Roleplay احترافي</p>
      <button class="btn-primary">انضم الآن</button>
    </div>
  </div>
</div>

<!-- CREATORS -->
<div id="creators" class="page">
  <div class="section">
    <div class="section-title">صناع المحتوى</div>
    <div class="card">صانع محتوى 1</div>
    <div class="card">صانع محتوى 2</div>
  </div>
</div>

<!-- LIVE -->
<div id="live" class="page">
  <div class="section">
    <div class="section-title">البث المباشر</div>
    <div class="card">لا يوجد بث حالياً</div>
  </div>
</div>

<!-- TEAM -->
<div id="team" class="page">
  <div class="section">
    <div class="section-title">الفريق</div>
    <div class="card">المالك - Owner</div>
    <div class="card">الإدارة</div>
  </div>
</div>

<!-- SHOP -->
<div id="shop" class="page">
  <div class="section">
    <div class="section-title">المتجر</div>
    <div class="card">VIP - 49</div>
    <div class="card">سيارة - 99</div>
  </div>
</div>

<!-- RULES -->
<div id="rules" class="page">
  <div class="section">
    <div class="section-title">القوانين</div>
    <div class="card">احترام الجميع</div>
    <div class="card">ممنوع RDM</div>
  </div>
</div>

</div>

<script>

function show(id,btn){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-links button').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  if(btn) btn.classList.add('active');
}

/* ADMIN */
function adminLogin(){
  let pass = prompt("ادخل كلمة المرور:");
  if(pass === "8901"){
    alert("تم الدخول كمشرف");
    openAdmin();
  } else {
    alert("خطأ");
  }
}

function openAdmin(){
  let panel = document.createElement("div");
  panel.className = "admin-panel";
  panel.innerHTML = `
    <h3 style="color:#1e5eff;margin-bottom:10px;">لوحة المشرف</h3>

    <button>تعديل المتجر</button>
    <button>تعديل الفريق</button>
    <button>تعديل صناع المحتوى</button>
    <button>تعديل البث</button>

    <button class="close-btn" onclick="this.parentElement.remove()">إغلاق</button>
  `;
  document.body.appendChild(panel);
}

</script>

</body>
</html>
