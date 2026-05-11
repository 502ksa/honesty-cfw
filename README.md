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

.navbar{
  position:fixed;top:0;left:0;width:100%;z-index:1000;
  display:flex;justify-content:space-between;align-items:center;
  padding:0 40px;height:65px;
  background:rgba(8,10,20,0.85);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(30,94,255,0.15);
}
.nav-logo{
  font-size:20px;font-weight:900;color:#fff;letter-spacing:1px;
}
.nav-logo span{color:#1e5eff;}
.nav-links{display:flex;gap:4px;align-items:center;}
.nav-links button{
  background:transparent;border:none;color:rgba(255,255,255,0.75);
  padding:8px 16px;border-radius:8px;font-size:14px;font-weight:500;
  cursor:pointer;font-family:'Tajawal',sans-serif;transition:all .25s;
}
.nav-links button:hover,.nav-links button.active{
  color:#fff;background:rgba(30,94,255,0.15);
}
.nav-shop{
  background:#1e5eff!important;color:#fff!important;
  padding:8px 20px!important;border-radius:8px;font-weight:700!important;
}
.nav-shop:hover{background:#1a50e0!important;transform:translateY(-1px);}

.container{width:100%;min-height:100vh;padding-top:65px;}

.page{display:none;}
.active{display:block;}

/* ===== HOME ===== */
.hero{
  position:relative;min-height:calc(100vh - 65px);
  display:flex;align-items:center;justify-content:center;
  text-align:center;overflow:hidden;
}
.hero-bg{
  position:absolute;inset:0;
  background:url('https://images.unsplash.com/photo-1520975916090-3105956dac38?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
  z-index:0;
}
.hero-bg::after{
  content:'';position:absolute;inset:0;
  background:linear-gradient(to bottom,rgba(5,7,18,0.55) 0%,rgba(5,7,18,0.75) 70%,#0a0c14 100%);
}
.hero-content{position:relative;z-index:1;max-width:780px;padding:0 20px;}
.hero-badge{
  display:inline-block;
  background:rgba(30,94,255,0.15);border:1px solid rgba(30,94,255,0.4);
  color:#7aaeff;padding:6px 18px;border-radius:50px;font-size:13px;font-weight:700;
  margin-bottom:22px;letter-spacing:1px;
}
.hero h1{font-size:clamp(2.8rem,7vw,5.5rem);font-weight:900;line-height:1.1;color:#fff;margin-bottom:8px;}
.hero h1 span{color:#1e5eff;}
.hero p{color:rgba(255,255,255,0.65);font-size:1.1rem;max-width:560px;margin:0 auto 32px;line-height:1.7;}
.hero-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;}
.btn-primary{
  background:#1e5eff;color:#fff;padding:14px 32px;border-radius:10px;
  border:none;font-weight:700;font-size:15px;cursor:pointer;
  font-family:'Tajawal',sans-serif;transition:all .25s;
}
.btn-primary:hover{background:#1a50e0;transform:translateY(-2px);box-shadow:0 8px 30px rgba(30,94,255,0.4);}
.btn-secondary{
  background:rgba(255,255,255,0.08);color:#fff;padding:14px 32px;border-radius:10px;
  border:1px solid rgba(255,255,255,0.15);font-weight:600;font-size:15px;cursor:pointer;
  font-family:'Tajawal',sans-serif;transition:all .25s;
}
.btn-secondary:hover{background:rgba(255,255,255,0.14);}
.stats{
  display:flex;justify-content:center;gap:60px;flex-wrap:wrap;
  margin-top:56px;padding:28px 0;
  border-top:1px solid rgba(255,255,255,0.07);
}
.stat-num{font-size:2rem;font-weight:900;}
.stat-label{font-size:12px;color:rgba(255,255,255,0.45);margin-top:2px;}

/* ===== FEATURES ===== */
.section{padding:80px 40px;max-width:1200px;margin:0 auto;}
.section-tag{display:block;color:#1e5eff;font-size:13px;font-weight:700;letter-spacing:2px;margin-bottom:10px;}
.section-title{font-size:2rem;font-weight:900;margin-bottom:12px;}
.section-sub{color:rgba(255,255,255,0.5);max-width:500px;line-height:1.7;}
.features-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px;margin-top:50px;}
.feature-card{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:16px;padding:28px;transition:all .3s;
}
.feature-card:hover{border-color:rgba(30,94,255,0.3);background:rgba(30,94,255,0.06);transform:translateY(-4px);}
.feature-icon{
  width:48px;height:48px;background:rgba(30,94,255,0.15);border-radius:12px;
  display:flex;align-items:center;justify-content:center;font-size:22px;margin-bottom:16px;
}
.feature-card h3{font-size:16px;font-weight:700;margin-bottom:8px;}
.feature-card p{color:rgba(255,255,255,0.5);font-size:14px;line-height:1.6;}

/* ===== CREATORS ===== */
.creators-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:20px;margin-top:50px;}
.creator-card{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:16px;padding:24px;text-align:center;transition:all .3s;
}
.creator-card:hover{border-color:rgba(30,94,255,0.3);transform:translateY(-4px);}
.creator-avatar{
  width:80px;height:80px;border-radius:50%;
  background:linear-gradient(135deg,#1e5eff,#0a2a7a);
  margin:0 auto 14px;display:flex;align-items:center;justify-content:center;
  font-size:28px;font-weight:900;border:2px solid rgba(30,94,255,0.3);
}
.creator-name{font-weight:700;font-size:16px;margin-bottom:6px;}
.creator-platform{
  font-size:12px;font-weight:600;padding:3px 10px;border-radius:50px;
  background:rgba(30,94,255,0.1);color:#7aaeff;
}

/* ===== LIVE ===== */
.live-stats-row{display:flex;gap:20px;flex-wrap:wrap;margin-bottom:40px;}
.live-stat{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:12px;padding:18px 28px;text-align:center;
}
.live-stat-num{font-size:1.8rem;font-weight:900;}
.live-stat-label{color:rgba(255,255,255,0.45);font-size:12px;margin-top:2px;}
.live-empty{
  background:rgba(255,255,255,0.03);border:1px solid rgba(255,255,255,0.06);
  border-radius:16px;padding:60px;text-align:center;color:rgba(255,255,255,0.3);font-size:15px;
}

/* ===== TEAM ===== */
.team-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:20px;margin-top:50px;}
.team-card{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:16px;padding:24px;text-align:center;transition:all .3s;
}
.team-card:hover{border-color:rgba(30,94,255,0.3);transform:translateY(-4px);}
.team-avatar{
  width:80px;height:80px;border-radius:50%;
  background:linear-gradient(135deg,#1e5eff,#0a2a7a);
  margin:0 auto 14px;display:flex;align-items:center;justify-content:center;
  font-size:26px;font-weight:900;border:2px solid rgba(30,94,255,0.3);
}
.team-name{font-weight:700;font-size:16px;margin-bottom:6px;}
.team-role{
  display:inline-block;font-size:12px;font-weight:600;padding:3px 12px;
  border-radius:50px;background:rgba(30,94,255,0.12);color:#7aaeff;
}

/* ===== SHOP ===== */
.shop-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:20px;margin-top:50px;}
.shop-card{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:16px;overflow:hidden;transition:all .3s;
}
.shop-card:hover{border-color:rgba(30,94,255,0.3);transform:translateY(-4px);}
.shop-img{
  height:150px;background:linear-gradient(135deg,rgba(30,94,255,0.2),rgba(10,20,60,0.8));
  display:flex;align-items:center;justify-content:center;font-size:40px;
}
.shop-body{padding:20px;}
.shop-name{font-weight:700;font-size:16px;margin-bottom:6px;}
.shop-desc{color:rgba(255,255,255,0.45);font-size:13px;margin-bottom:16px;line-height:1.5;}
.shop-footer{display:flex;align-items:center;justify-content:space-between;}
.shop-price{font-size:18px;font-weight:900;color:#1e5eff;}

/* ===== RULES ===== */
.rules-list{margin-top:40px;display:flex;flex-direction:column;gap:14px;}
.rule-item{
  background:rgba(255,255,255,0.04);border:1px solid rgba(255,255,255,0.07);
  border-radius:12px;padding:18px 24px;display:flex;align-items:flex-start;gap:14px;transition:border-color .25s;
}
.rule-item:hover{border-color:rgba(30,94,255,0.25);}
.rule-num{
  min-width:32px;height:32px;background:rgba(30,94,255,0.15);border-radius:8px;
  display:flex;align-items:center;justify-content:center;font-weight:700;font-size:13px;color:#7aaeff;
}
.rule-text h4{font-size:15px;font-weight:700;margin-bottom:4px;}
.rule-text p{color:rgba(255,255,255,0.5);font-size:13px;line-height:1.5;}

.footer{
  text-align:center;padding:30px;color:rgba(255,255,255,0.2);font-size:13px;
  border-top:1px solid rgba(255,255,255,0.05);
}
</style>
</head>
<body>

<nav class="navbar">
  <div class="nav-logo"><span>Honesty</span> CFW</div>
  <div class="nav-links">
    <button class="active" onclick="show('home',this)">الرئيسية</button>
    <button onclick="show('creators',this)">صناع المحتوى</button>
    <button onclick="show('live',this)">البث المباشر</button>
    <button onclick="show('team',this)">الفريق</button>
    <button onclick="show('shop',this)" class="nav-shop">🛒 المتجر</button>
    <button onclick="show('rules',this)">القوانين</button>
  </div>
</nav>

<div class="container">

<!-- الرئيسية -->
<div id="home" class="page active">
  <div class="hero">
    <div class="hero-bg"></div>
    <div class="hero-content">
      <div class="hero-badge">رقم 1 كأفضل سيرفر Roleplay احترافي</div>
      <h1>Honesty <span>CFW</span></h1>
      <p>أقوى سيرفر Roleplay احترافي — انضم لأكبر مجتمع وعش تجربة لا تُنسى</p>
      <div class="hero-btns">
        <button class="btn-primary">▶ انضم الآن</button>
        <button class="btn-secondary">اعرف المزيد ›</button>
      </div>
      <div class="stats">
        <div><div class="stat-num">300K+</div><div class="stat-label">لاعب مسجل</div></div>
        <div><div class="stat-num">50+</div><div class="stat-label">صانع محتوى</div></div>
        <div><div class="stat-num">24/7</div><div class="stat-label">دعم فني</div></div>
        <div><div class="stat-num">5+</div><div class="stat-label">سنوات خبرة</div></div>
      </div>
    </div>
  </div>
  <div class="section">
    <span class="section-tag">✦ مميزاتنا</span>
    <h2 class="section-title">لماذا Honesty CFW؟</h2>
    <p class="section-sub">اكتشف ما يجعلنا الخيار الأول لمحبي تجارب الـ Roleplay</p>
    <div class="features-grid">
      <div class="feature-card"><div class="feature-icon">🎮</div><h3>تجربة Roleplay احترافية</h3><p>عالم مليء بالتفاصيل والأحداث مع قصص لا تُنسى</p></div>
      <div class="feature-card"><div class="feature-icon">👥</div><h3>مجتمع متميز</h3><p>آلاف اللاعبين في بيئة محترمة وعادلة للجميع</p></div>
      <div class="feature-card"><div class="feature-icon">🛡️</div><h3>إدارة قوية</h3><p>فريق متخصص يعمل على راحة اللاعبين وحل المشكلات</p></div>
      <div class="feature-card"><div class="feature-icon">⚡</div><h3>سيرفر مستقر</h3><p>أداء عالي وانتظام في التشغيل على مدار اليوم</p></div>
      <div class="feature-card"><div class="feature-icon">🎬</div><h3>محتوى متجدد</h3><p>فعاليات وتحديثات دورية تضمن تجربة جديدة دائماً</p></div>
      <div class="feature-card"><div class="feature-icon">💎</div><h3>مميزات حصرية</h3><p>رتب وسيارات ومزايا خاصة لتميّز تجربتك</p></div>
    </div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

<!-- صناع المحتوى -->
<div id="creators" class="page">
  <div class="section">
    <span class="section-tag">✦ صناع المحتوى</span>
    <h2 class="section-title">تعرفوا على صناع المحتوى</h2>
    <p class="section-sub">صناع محتوى مميزون يمثلون Honesty CFW</p>
    <div class="creators-grid">
      <div class="creator-card"><div class="creator-avatar">ع</div><div class="creator-name">العضو 1</div><span class="creator-platform">YouTube</span></div>
      <div class="creator-card"><div class="creator-avatar">م</div><div class="creator-name">العضو 2</div><span class="creator-platform">Kick</span></div>
      <div class="creator-card"><div class="creator-avatar">س</div><div class="creator-name">العضو 3</div><span class="creator-platform">Twitch</span></div>
    </div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

<!-- البث المباشر -->
<div id="live" class="page">
  <div class="section">
    <span class="section-tag">🔴 البث المباشر</span>
    <h2 class="section-title">جميع البثوث المباشرة</h2>
    <p class="section-sub">شاهد صناع محتوى Honesty CFW مباشرةً</p>
    <div class="live-stats-row">
      <div class="live-stat"><div class="live-stat-num">0</div><div class="live-stat-label">بث مباشر</div></div>
      <div class="live-stat"><div class="live-stat-num">0</div><div class="live-stat-label">إجمالي المشاهدين</div></div>
    </div>
    <div class="live-empty">لا يوجد بث مباشر الآن — تابعنا لاحقاً 🎬</div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

<!-- الفريق -->
<div id="team" class="page">
  <div class="section">
    <span class="section-tag">✦ الفريق</span>
    <h2 class="section-title">الفريق وراء Honesty CFW</h2>
    <p class="section-sub">تعرفوا على الفريق الذي يبني لكم أفضل تجربة</p>
    <div class="team-grid">
      <div class="team-card"><div class="team-avatar">م</div><div class="team-name">المالك</div><span class="team-role">Owner</span></div>
      <div class="team-card"><div class="team-avatar">م</div><div class="team-name">المؤسس</div><span class="team-role">Founder</span></div>
      <div class="team-card"><div class="team-avatar">إ</div><div class="team-name">الإدارة</div><span class="team-role">Staff</span></div>
    </div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

<!-- المتجر -->
<div id="shop" class="page">
  <div class="section">
    <span class="section-tag">🛒 المتجر</span>
    <h2 class="section-title">متجر Honesty CFW</h2>
    <p class="section-sub">رتب + سيارات + مزايا حصرية</p>
    <div class="shop-grid">
      <div class="shop-card">
        <div class="shop-img">👑</div>
        <div class="shop-body">
          <div class="shop-name">رتبة VIP</div>
          <div class="shop-desc">تمتع بمميزات حصرية داخل السيرفر</div>
          <div class="shop-footer"><span class="shop-price">49 ريال</span><button class="btn-primary" style="padding:8px 18px;font-size:13px;">شراء</button></div>
        </div>
      </div>
      <div class="shop-card">
        <div class="shop-img">🚗</div>
        <div class="shop-body">
          <div class="shop-name">سيارة مخصصة</div>
          <div class="shop-desc">سيارة خاصة بك داخل اللعبة</div>
          <div class="shop-footer"><span class="shop-price">99 ريال</span><button class="btn-primary" style="padding:8px 18px;font-size:13px;">شراء</button></div>
        </div>
      </div>
      <div class="shop-card">
        <div class="shop-img">💎</div>
        <div class="shop-body">
          <div class="shop-name">باقة مميزة</div>
          <div class="shop-desc">مجموعة كاملة من المزايا الحصرية</div>
          <div class="shop-footer"><span class="shop-price">199 ريال</span><button class="btn-primary" style="padding:8px 18px;font-size:13px;">شراء</button></div>
        </div>
      </div>
    </div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

<!-- القوانين -->
<div id="rules" class="page">
  <div class="section">
    <span class="section-tag">📋 القوانين</span>
    <h2 class="section-title">قوانين Honesty CFW</h2>
    <p class="section-sub">يرجى الالتزام بجميع القوانين لضمان تجربة ممتعة للجميع</p>
    <div class="rules-list">
      <div class="rule-item"><div class="rule-num">1</div><div class="rule-text"><h4>احترام الجميع</h4><p>يجب احترام جميع اللاعبين والإدارة داخل السيرفر</p></div></div>
      <div class="rule-item"><div class="rule-num">2</div><div class="rule-text"><h4>ممنوع RDM</h4><p>القتل العشوائي بدون سبب رول بلاي مقبول ممنوع كلياً</p></div></div>
      <div class="rule-item"><div class="rule-num">3</div><div class="rule-text"><h4>ممنوع VDM</h4><p>استخدام السيارة كسلاح بدون مبرر ممنوع</p></div></div>
      <div class="rule-item"><div class="rule-num">4</div><div class="rule-text"><h4>الالتزام بالرول بلاي</h4><p>يجب البقاء داخل شخصيتك طوال وقت اللعب</p></div></div>
      <div class="rule-item"><div class="rule-num">5</div><div class="rule-text"><h4>ممنوع الغش والاستغلال</h4><p>أي استخدام لبرامج أو ثغرات للتلاعب بالسيرفر يؤدي للحظر الدائم</p></div></div>
    </div>
  </div>
  <div class="footer">© 2025 Honesty CFW — جميع الحقوق محفوظة</div>
</div>

</div>

<script>
function show(id, btn){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-links button').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  if(btn) btn.classList.add('active');
  window.scrollTo(0,0);
}
</script>

</body>
</html>
