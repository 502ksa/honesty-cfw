<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');

html, body{
    margin:0;
    padding:0;
    height:100%;
    width:100%;
    overflow:hidden;
    font-family:'Cairo', sans-serif;
    background:black;
}

/* خلفية سينمائية */
.bg{
    position:fixed;
    width:100%;
    height:100%;
    background: url('https://images.unsplash.com/photo-1520975922284-9c7f1b8c2a9f?auto=format&fit=crop&w=1600&q=80');
    background-size:cover;
    background-position:center;
    filter:brightness(0.35);
    z-index:-2;
}

/* طبقة تأثير */
.overlay{
    position:fixed;
    width:100%;
    height:100%;
    background: radial-gradient(circle, rgba(0,0,0,0.2), rgba(0,0,0,0.85));
    z-index:-1;
}

/* Navbar */
.navbar{
    position:fixed;
    top:0;
    width:100%;
    display:flex;
    justify-content:center;
    gap:10px;
    padding:15px;
    background:rgba(10,15,30,0.4);
    backdrop-filter: blur(12px);
    border-bottom:1px solid rgba(255,255,255,0.08);
}

.navbar button{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.1);
    color:white;
    padding:10px 16px;
    border-radius:12px;
    cursor:pointer;
    transition:0.3s;
}

.navbar button:hover{
    background:#1e5eff;
    transform:translateY(-2px);
}

/* الصفحات */
.container{
    position:absolute;
    top:70px;
    width:100%;
    height:calc(100% - 70px);
}

.page{
    display:none;
    height:100%;
    padding:60px;
    animation:fade 0.5s ease;
}

.active{
    display:flex;
    flex-direction:column;
    justify-content:center;
}

/* كرت رئيسي */
.card{
    background:rgba(255,255,255,0.05);
    border:1px solid rgba(255,255,255,0.1);
    padding:25px;
    border-radius:18px;
    backdrop-filter: blur(10px);
    max-width:600px;
    box-shadow:0 0 30px rgba(0,0,0,0.4);
}

/* عنوان */
h1{
    color:#4aa3ff;
    font-size:40px;
    margin:0 0 15px 0;
}

/* نص */
p{
    color:#ddd;
}

/* انيميشن */
@keyframes fade{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

/* Glow */
.glow{
    color:#4aa3ff;
    text-shadow:0 0 10px #1e5eff;
}
</style>

</head>

<body>

<div class="bg"></div>
<div class="overlay"></div>

<!-- Navbar -->
<div class="navbar">
    <button onclick="show('home')">الرئيسية</button>
    <button onclick="show('rules')">القوانين</button>
    <button onclick="show('creators')">صناع المحتوى</button>
    <button onclick="show('apply')">التقديم</button>
    <button onclick="show('info')">المعلومات</button>
</div>

<!-- الصفحات -->
<div class="container">

<!-- الرئيسية -->
<div id="home" class="page active">
    <div class="card">
        <h1 class="glow">Honesty CFW</h1>
        <p>أقوى تجربة Roleplay احترافية — سيرفر مبني بأسلوب واقعي ونظام متكامل.</p>
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
        • أي مخالفة = عقوبة فورية
        </p>
    </div>
</div>

<!-- صناع المحتوى -->
<div id="creators" class="page">
    <div class="card">
        <h1>صناع المحتوى</h1>
        <p>
        إذا كنت صانع محتوى وتبي تعاون مع السيرفر، تواصل مع الإدارة عبر الديسكورد.
        </p>
    </div>
</div>

<!-- التقديم -->
<div id="apply" class="page">
    <div class="card">
        <h1>التقديم</h1>
        <p>
        التقديم مفتوح حالياً للمافيا والإدارة<br>
        كن جزء من أقوى مجتمع RP.
        </p>
    </div>
</div>

<!-- المعلومات -->
<div id="info" class="page">
    <div class="card">
        <h1>المعلومات</h1>
        <p>
        سيرفر احترافي — فعاليات مستمرة — نظام اقتصادي — عصابات — وظائف — إدارة قوية.
        </p>
    </div>
</div>

</div>

<script>
function show(id){
    let pages = document.querySelectorAll('.page');
    pages.forEach(p => p.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
