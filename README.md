<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Cairo', sans-serif;
}

html,body{
  width:100%;
  height:100%;
  overflow:hidden;
  background:#050b18;
}

/* خلفية */
.bg{
  position:fixed;
  width:100%;
  height:100%;
  background:url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1600&q=80');
  background-size:cover;
  background-position:center;
  filter:brightness(0.35);
  z-index:-2;
}

.overlay{
  position:fixed;
  width:100%;
  height:100%;
  background:radial-gradient(circle, rgba(0,0,0,0.2), rgba(0,0,0,0.9));
  z-index:-1;
}

/* navbar */
.navbar{
  position:fixed;
  top:0;
  width:100%;
  display:flex;
  justify-content:center;
  gap:10px;
  padding:15px;
  background:rgba(10,15,30,0.35);
  backdrop-filter:blur(12px);
  border-bottom:1px solid rgba(255,255,255,0.08);
}

.navbar button{
  background:rgba(255,255,255,0.05);
  border:1px solid rgba(255,255,255,0.1);
  color:white;
  padding:10px 14px;
  border-radius:12px;
  cursor:pointer;
  transition:0.3s;
}

.navbar button:hover{
  background:#1e5eff;
}

/* container */
.container{
  position:absolute;
  top:70px;
  width:100%;
  height:calc(100% - 70px);
}

/* pages */
.page{
  display:none;
  height:100%;
  padding:60px;
  animation:fade .4s ease;
}

.active{
  display:flex;
  align-items:center;
}

/* card */
.card{
  background:rgba(255,255,255,0.06);
  border:1px solid rgba(255,255,255,0.1);
  padding:25px;
  border-radius:18px;
  backdrop-filter:blur(12px);
  max-width:700px;
}

h1{
  color:#4aa3ff;
  margin-bottom:10px;
}

/* زر */
.btn{
  display:inline-block;
  margin-top:15px;
  padding:10px 15px;
  background:#1e5eff;
  color:white;
  border-radius:10px;
  text-decoration:none;
}

@keyframes fade{
  from{opacity:0; transform:translateY(20px);}
  to{opacity:1; transform:translateY(0);}
}
</style>

</head>

<body>

<div class="bg"></div>
<div class="overlay"></div>

<!-- NAV -->
<div class="navbar">
  <button onclick="show('home')">الرئيسية</button>
  <button onclick="show('creators')">صناع المحتوى</button>
  <button onclick="show('live')">البث المباشر</button>
  <button onclick="show('team')">الفريق</button>
  <button onclick="show('shop')">المتجر</button>
  <button onclick="show('rules')">القوانين</button>
</div>

<div class="container">

<!-- الرئيسية -->
<div id="home" class="page active">
  <div class="card">
    <h1>Honesty CFW</h1>
    <p>أقوى سيرفر Roleplay احترافي — نظام متكامل وتجربة واقعية.</p>

    <a class="btn" onclick="show('team')">اعرف المزيد</a>
  </div>
</div>

<!-- صناع المحتوى -->
<div id="creators" class="page">
  <div class="card">
    <h1>صناع المحتوى</h1>
    <p>نرحب بجميع صناع المحتوى للتعاون مع السيرفر.</p>
  </div>
</div>

<!-- البث المباشر -->
<div id="live" class="page">
  <div class="card">
    <h1>البث المباشر</h1>
    <p>هنا يتم عرض فعاليات السيرفر والبثوث المباشرة.</p>
  </div>
</div>

<!-- الفريق -->
<div id="team" class="page">
  <div class="card">
    <h1>الفريق</h1>
    <p>
salem    </p>
  </div>
</div>

<!-- المتجر -->
<div id="shop" class="page">
  <div class="card">
    <h1>المتجر</h1>
    <p>شراء رتب — سيارات — مزايا خاصة داخل السيرفر.</p>
  </div>
</div>

<!-- القوانين -->
<div id="rules" class="page">
  <div class="card">
    <h1>القوانين</h1>
    <p>
      • احترام الجميع<br>
      • ممنوع RDM / VDM<br>
      • الالتزام بالرول بلاي<br>
      • أي مخالفة = عقوبة
    </p>
  </div>
</div>

</div>

<script>
function show(id){
  let pages=document.querySelectorAll('.page');
  pages.forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
