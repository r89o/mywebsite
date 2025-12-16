<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>خلية البيئة الذكية</title>

<style>
body{
    font-family: Arial, sans-serif;
    background:#F1F8F6;
    text-align:center;
    margin:0;
    padding:0;
    color:#263238;
}

header{
    background:#2E7D32;
    color:white;
    padding:25px;
}

header img{
    width:90%;
    max-width:500px;
    border-radius:15px;
    margin-top:15px;
}

section{
    background:white;
    margin:20px;
    padding:20px;
    border-radius:15px;
    box-shadow:0 4px 10px rgba(0,0,0,0.08);
}

.light{
    width:110px;
    height:110px;
    border-radius:50%;
    margin:15px auto;
}

.green{ background:#4CAF50; }
.yellow{ background:#FFEB3B; }
.red{ background:#F44336; }

button{
    padding:12px 25px;
    font-size:16px;
    border:none;
    border-radius:12px;
    cursor:pointer;
    background:#2E7D32;
    color:white;
}

button:hover{
    background:#1B5E20;
}

img.section-img{
    width:100%;
    max-width:400px;
    border-radius:15px;
    margin-top:15px;
}

.contact{
    background:#A5D6A7;
    border-radius:15px;
    padding:20px;
}

footer{
    background:#2E7D32;
    color:white;
    padding:12px;
    font-size:14px;
}
</style>
</head>

<body>

<header>
    <h1>🌱 خلية البيئة الذكية</h1>
    <p>حل ذكي ومستدام لممرات المدارس</p>
    <img src="https://images.unsplash.com/photo-1596496056212-0c05c4524e6a?auto=format&fit=crop&w=800&q=80" alt="ممر مدرسة نظيف وجهاز ذكي">
</header>

<section>
    <h2>نبذة عن المشروع</h2>
    <p>
        خلية البيئة الذكية هي جهاز يركب في ممرات المدارس لمراقبة جودة الهواء، 
        درجة الحرارة، والإضاءة والازدحام. يعرض الجهاز الحالة عبر ألوان ضوئية ويقدم حلول تلقائية لتحسين البيئة.
    </p>
    <img class="section-img" src="https://images.unsplash.com/photo-1581093458792-c0d6c22b6d84?auto=format&fit=crop&w=800&q=80" alt="جهاز ذكي لمراقبة البيئة في المدرسة">
</section>

<section>
    <h2>دلالات الألوان</h2>

    <div class="light green"></div>
    <p>🟢 البيئة آمنة – لا حاجة لأي تدخل</p>

    <div class="light yellow"></div>
    <p>🟡 تنبيه – تشغيل التهوية تلقائياً</p>

    <div class="light red"></div>
    <p>🔴 خطر – إنذار وإشعار فوري للإدارة</p>
</section>

<section>
    <h2>محاكاة عمل الجهاز</h2>
    <p>اضغطي الزر لتغيير الحالة</p>
    <button onclick="changeStatus()">تغيير الحالة</button>
    <div id="statusLight" class="light green"></div>
    <p id="statusText">🟢 البيئة مستقرة</p>
</section>

<section class="contact">
    <h2>📞 تواصل معنا</h2>
    <p>خدمة العملاء متوفرة للمدارس والجهات التعليمية</p>
    <p>📱 الهاتف: 0535997762</p>
    <p>📧 البريد الإلكتروني: retajalqahtani74@gmail.com</p>
    <p>📷 QR Code للموقع:</p>
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://example.com" alt="QR Code" style="margin-top:10px;">
</section>

<footer>
    مشروع مدرسي | خلية البيئة الذكية 🌿
</footer>

<script>
let state = 0;

function changeStatus(){
    const light = document.getElementById("statusLight");
    const text = document.getElementById("statusText");

    if(state === 0){
        light.className = "light yellow";
        text.innerHTML = "🟡 تنبيه: تشغيل التهوية تلقائياً";
        state = 1;
    } 
    else if(state === 1){
        light.className = "light red";
        text.innerHTML = "🔴 خطر: إنذار + إشعار للإدارة";
        state = 2;
    } 
    else{
        light.className = "light green";
        text.innerHTML = "🟢 البيئة مستقرة";
        state = 0;
    }
}
</script>

</body>
</html>
