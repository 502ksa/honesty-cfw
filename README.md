<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<style>
body{
    margin:0;
    font-family: Arial;
    background:#071a33;
    color:white;
}

/* الشريط العلوي */
.navbar{
    display:flex;
    justify-content:center;
    gap:10px;
    background:#0c2a4d;
    padding:15px;
    position:sticky;
    top:0;
}

.navbar button{
    background:#1e5eff;
    border:none;
    padding:10px 15px;
    color:white;
    border-radius:8px;
    cursor:pointer;
}

.navbar button:hover{
    background:#144bd1;
}

/* الأقسام */
.section{
    display:none;
    padding:30px;
    animation: fade 0.3s ease-in-out;
}

.active{
    display:block;
}

h1{
    color:#4aa3ff;
}

.box{
    background:#0f2f55;
    padding:15px;
    border-radius:12px;
    margin-top:10px;
}

/* حركة بسيطة */
@keyframes fade{
    from{opacity:0; transform:translateY(10px);}
    to{opacity:1; transform:translateY(0);}
}
</style>

</head>
<body>

<!-- الأزرار -->
<div class="navbar">
    <button onclick="show('home')">الرئيسية</button>
    <button onclick="show('rules')">القوانين</button>
    <button onclick="show('creators')">صناع المحتوى</button>
    <button onclick="show('apply')">التقديم</button>
    <button onclick="show('info')">المعلومات</button>
</div>

<!-- الصفحة الرئيسية -->
<div id="home" class="section active">
    <h1>Honesty CFW</h1>
    <div class="box">
        مرحبًا بك في سيرفر Honesty CFW  
        تجربة Roleplay احترافية ومميزة.
    </div>
</div>

<!-- القوانين -->
<div id="rules" class="section">
    <h1>القوانين</h1>
    <div class="box">
        1- احترام الجميع<br>
        2- ممنوع السب أو التخريب<br>
        3- الالتزام بالرول بلاي<br>
        4- مخالفة القوانين = عقوبة
    </div>
</div>

<!-- صناع المحتوى -->
<div id="creators" class="section">
    <h1>صناع المحتوى</h1>
    <div class="box">
        إذا تبي تكون صانع محتوى في السيرفر:<br>
        تواصل مع الإدارة وقدم طلبك.
    </div>
</div>

<!-- التقديم -->
<div id="apply" class="section">
    <h1>التقديم</h1>
    <div class="box">
        التقديم مفتوح حالياً للمافيا والإدارة<br>
        تابع الديسكورد للتفاصيل.
    </div>
</div>

<!-- المعلومات -->
<div id="info" class="section">
    <h1>المعلومات</h1>
    <div class="box">
        سيرفر مبني بشكل احترافي مع فعاليات مستمرة ونظام قوي.
    </div>
</div>

<script>
function show(id){
    let sections = document.querySelectorAll('.section');
    sections.forEach(s => s.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
