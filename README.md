<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Honesty CFW</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: #0b1a2f;
    color: white;
}

/* الهيدر */
header {
    background: #0f2d4f;
    padding: 15px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header h1 {
    margin: 0;
    color: #4aa3ff;
    font-size: 22px;
}

/* زر */
button {
    background: #1e5eff;
    border: none;
    padding: 10px 15px;
    color: white;
    border-radius: 8px;
    cursor: pointer;
}

button:hover {
    background: #144bd1;
}

/* القائمة */
.container {
    padding: 20px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 15px;
}

.card {
    background: #102a4a;
    padding: 15px;
    border-radius: 12px;
    border: 1px solid #1e5eff33;
}

.card h3 {
    margin-top: 0;
    color: #4aa3ff;
}
</style>

</head>
<body>

<header>
    <h1>Honesty CFW</h1>
    <button onclick="alert('تم الدخول')">دخول السيرفر</button>
</header>

<div class="container">

    <div class="card">
        <h3>القوانين</h3>
        <p>هنا يتم عرض قوانين السيرفر بشكل مرتب.</p>
    </div>

    <div class="card">
        <h3>التقديم</h3>
        <p>التقديم مفتوح حالياً للمافيا والإدارة.</p>
    </div>

    <div class="card">
        <h3>المعلومات</h3>
        <p>سيرفر Roleplay احترافي مع نظام متكامل.</p>
    </div>

</div>

</body>
</html>
