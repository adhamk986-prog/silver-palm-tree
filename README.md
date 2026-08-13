<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>قيّم نفسك بنفسك | مدرسة الموالح الخاصة</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Reem+Kufi:wght@400..700&family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --cream:#fbf1e0;
    --cream-2:#f3e6cd;
    --ink:#2a2420;
    --ink-soft:#5a5044;
    --teal:#1e6e76;
    --teal-2:#2e8a93;
    --olive:#8fa23e;
    --orange:#de8b3b;
    --plum:#6b4a73;
    --line:#e3d3ad;
    --shadow:0 22px 55px rgba(42,36,32,0.22);
  }
  *{box-sizing:border-box;}
  html,body{margin:0;padding:0;}
  body{
    min-height:100vh;
    background:
      radial-gradient(circle at 12% 0%, rgba(222,139,59,0.14), transparent 42%),
      radial-gradient(circle at 90% 100%, rgba(30,110,118,0.14), transparent 45%),
      var(--cream);
    font-family:'Tajawal', sans-serif;
    color:var(--ink);
    display:flex;
    flex-direction:column;
    align-items:center;
    padding:20px 16px 40px;
  }

  /* ===== Header ===== */
  .school-header{
    width:100%;
    max-width:680px;
    display:flex;
    align-items:center;
    gap:14px;
    padding:6px 4px 20px;
  }
  .school-logo{
    width:56px;
    height:56px;
    border-radius:50%;
    object-fit:cover;
    box-shadow:0 6px 16px rgba(42,36,32,0.25);
    border:2px solid #fff;
    flex-shrink:0;
  }
  .school-titles{ line-height:1.35; }
  .school-titles .ar{
    font-family:'Reem Kufi', sans-serif;
    font-size:19px;
    font-weight:700;
    color:var(--ink);
  }
  .school-titles .en{
    font-size:12px;
    color:var(--ink-soft);
    letter-spacing:0.5px;
  }

  .stage{ width:100%; max-width:680px; }

  .card{
    background: linear-gradient(180deg, #fffdf8, var(--cream-2));
    border-radius:20px;
    box-shadow:var(--shadow);
    padding:38px 32px;
    position:relative;
    overflow:hidden;
    border:1px solid rgba(107,74,115,0.18);
  }
  .card::before{
    content:"";
    position:absolute;
    inset:0;
    height:6px;
    background:linear-gradient(90deg, var(--teal), var(--olive), var(--orange), var(--plum));
  }

  .eyebrow{
    font-size:12.5px;
    letter-spacing:2px;
    color:var(--orange);
    font-weight:700;
    text-transform:uppercase;
    display:block;
    margin-bottom:8px;
  }
  h1{
    font-family:'Reem Kufi', sans-serif;
    font-size:36px;
    margin:0 0 10px;
    color:var(--ink);
    line-height:1.3;
  }
  .subtitle{
    font-size:15.5px;
    color:var(--ink-soft);
    margin:0 0 26px;
  }

  label{
    display:block;
    font-weight:700;
    font-size:13.5px;
    margin:16px 0 6px;
    color:var(--ink-soft);
  }
  input[type="text"], input[type="email"]{
    width:100%;
    padding:13px 14px;
    border-radius:11px;
    border:1.5px solid var(--line);
    background:rgba(255,255,255,0.65);
    font-family:'Tajawal', sans-serif;
    font-size:15px;
    color:var(--ink);
    outline:none;
    transition:border-color .2s, box-shadow .2s;
  }
  input:focus{
    border-color:var(--teal);
    box-shadow:0 0 0 3px rgba(30,110,118,0.16);
  }
  .hint{ font-size:12px; color:var(--ink-soft); opacity:0.8; margin-top:4px; }

  /* photo upload */
  .photo-row{ display:flex; align-items:center; gap:16px; margin-top:16px; }
  .photo-frame{
    width:74px; height:74px; border-radius:50%; flex-shrink:0;
    border:2px dashed var(--line); background:rgba(255,255,255,0.55);
    display:flex; align-items:center; justify-content:center;
    overflow:hidden; position:relative;
  }
  .photo-frame img{ width:100%; height:100%; object-fit:cover; }
  .photo-frame .ph-icon{ font-size:24px; color:var(--ink-soft); opacity:0.5; }
  .photo-actions{ flex:1; }
  .photo-actions input[type="file"]{ display:none; }
  .photo-btn{
    display:inline-block; font-size:13px; font-weight:700; color:var(--teal);
    background:rgba(30,110,118,0.1); border:1.5px solid rgba(30,110,118,0.35);
    border-radius:10px; padding:9px 14px; cursor:pointer; transition:all .15s ease;
  }
  .photo-btn:hover{ background:rgba(30,110,118,0.18); }
  .photo-remove{
    font-size:12px; color:var(--orange); font-weight:700; cursor:pointer;
    background:none; border:none; margin-inline-start:10px; text-decoration:underline;
    display:none;
  }

  /* student mini badge shown during quiz + result */
  .student-badge{
    display:flex; align-items:center; gap:10px; margin-bottom:16px;
    padding:8px 10px; background:rgba(255,255,255,0.5);
    border:1px solid var(--line); border-radius:12px;
  }
  .student-badge img{
    width:38px; height:38px; border-radius:50%; object-fit:cover;
    border:1.5px solid #fff; box-shadow:0 3px 8px rgba(42,36,32,0.2); flex-shrink:0;
  }
  .student-badge .sb-icon{
    width:38px; height:38px; border-radius:50%; flex-shrink:0;
    background:rgba(107,74,115,0.12); color:var(--plum);
    display:flex; align-items:center; justify-content:center; font-size:16px; font-weight:800;
  }
  .student-badge .sb-info{ line-height:1.35; overflow:hidden; }
  .student-badge .sb-name{ font-size:13.5px; font-weight:800; color:var(--ink); }
  .student-badge .sb-meta{ font-size:11.5px; color:var(--ink-soft); }

  .timestamp-line{
    font-size:12.5px; color:var(--ink-soft); text-align:center; margin-top:6px; opacity:0.85;
  }

  .btn{
    appearance:none; border:none; cursor:pointer;
    font-family:'Tajawal', sans-serif; font-weight:800; font-size:15.5px;
    border-radius:12px; padding:14px 22px;
    transition:transform .15s ease, box-shadow .15s ease, opacity .2s ease;
  }
  .btn:focus-visible{ outline:3px solid var(--teal); outline-offset:2px; }
  .btn-primary{
    background:linear-gradient(180deg, var(--teal-2), var(--teal));
    color:#fff; width:100%; margin-top:24px;
    box-shadow:0 12px 26px rgba(30,110,118,0.32);
  }
  .btn-primary:hover{ transform:translateY(-2px); }
  .btn-primary:disabled{ opacity:0.45; cursor:not-allowed; transform:none; box-shadow:none; }
  .btn-ghost{
    background:transparent; color:var(--ink-soft); border:1.5px solid var(--line);
  }
  .btn-ghost:hover{ border-color:var(--orange); color:var(--orange); }

  /* progress - book pages */
  .book-progress{
    display:flex; align-items:center; gap:14px; margin-bottom:22px;
  }
  .book-progress svg{ flex-shrink:0; }
  .folio-label{
    font-family:'Reem Kufi', sans-serif;
    font-size:15px; color:var(--ink-soft); white-space:nowrap;
  }
  .folio-track{
    flex:1; height:7px; background:rgba(42,36,32,0.1);
    border-radius:7px; overflow:hidden;
  }
  .folio-fill{
    height:100%;
    background:linear-gradient(90deg, var(--teal), var(--olive), var(--orange));
    border-radius:7px; transition:width .4s ease;
  }

  .q-type{
    display:inline-block; font-size:11.5px; font-weight:800;
    color:var(--plum); background:rgba(107,74,115,0.12);
    padding:4px 10px; border-radius:20px; margin-bottom:10px;
  }
  .q-text{ font-size:21px; font-weight:800; line-height:1.6; margin:6px 0 22px; color:var(--ink); }
  .options{ display:flex; flex-direction:column; gap:12px; }
  .opt{
    text-align:right; background:rgba(255,255,255,0.55);
    border:1.5px solid var(--line); border-radius:12px;
    padding:14px 16px; font-size:15px; font-weight:600; color:var(--ink);
    cursor:pointer; transition:all .15s ease;
  }
  .opt:hover{ border-color:var(--teal); background:rgba(46,138,147,0.10); }
  .opt.selected{
    border-color:var(--teal); background:rgba(46,138,147,0.20);
    box-shadow:0 0 0 2px rgba(30,110,118,0.22) inset;
  }
  .tf-row{ display:flex; gap:12px; }
  .tf-row .opt{ flex:1; text-align:center; }

  .nav-row{ display:flex; justify-content:space-between; margin-top:26px; }
  .btn-next:disabled{ opacity:0.4; cursor:not-allowed; }

  /* result */
  .result-wrap{ text-align:center; }
  .medal{ width:150px; height:170px; margin:0 auto 6px; }
  .level-name{ font-family:'Reem Kufi', sans-serif; font-size:30px; margin:6px 0 2px; }
  .lvl-teal{ color:var(--teal); }
  .lvl-olive{ color:var(--olive); }
  .lvl-orange{ color:var(--orange); }
  .lvl-plum{ color:var(--plum); }
  .score-line{ font-size:15.5px; color:var(--ink-soft); margin-bottom:20px; }

  .breakdown{
    text-align:right; background:rgba(42,36,32,0.05);
    border-radius:12px; padding:16px 18px; margin-top:16px;
    font-size:13.5px; max-height:200px; overflow-y:auto;
  }
  .breakdown-item{
    display:flex; justify-content:space-between; gap:10px; padding:7px 0;
    border-bottom:1px dashed rgba(42,36,32,0.15);
  }
  .breakdown-item:last-child{ border-bottom:none; }
  .tag-ok{ color:var(--teal); font-weight:800; }
  .tag-no{ color:var(--orange); font-weight:800; }

  .send-box{
    margin-top:26px; text-align:right;
    background:rgba(30,110,118,0.06);
    border:1px dashed rgba(30,110,118,0.3);
    border-radius:14px; padding:18px 18px 20px;
  }
  .send-box .send-title{
    font-family:'Reem Kufi', sans-serif; font-size:16px;
    color:var(--teal); margin-bottom:10px;
  }
  .status-msg{
    margin-top:10px; font-size:13.5px; font-weight:700; display:none;
  }
  .status-ok{ color:var(--teal); }
  .status-err{ color:#b23a3a; }

  .footer-note{
    text-align:center; font-size:12px; color:var(--ink-soft); opacity:0.65; margin-top:20px;
  }

  @media (max-width:480px){
    .card{ padding:26px 18px; }
    h1{ font-size:28px; }
    .q-text{ font-size:18px; }
  }
  @media (prefers-reduced-motion: reduce){ *{ transition:none !important; animation:none !important; } }
</style>
</head>
<body>

<div class="school-header">
  <img class="school-logo" src="data:image/jpeg;base64,PASTE_LOGO_BASE64_HERE" alt="شعار المدرسة">
  <div class="school-titles">
    <div class="ar">مدرسة الموالح الخاصة</div>
    <div class="en">AL-MAWALEH PRIVATE SCHOOL</div>
  </div>
</div>

<div class="stage">

  <!-- شاشة البداية -->
  <div class="card" id="screen-start">
    <span class="eyebrow">تقييم ذاتي · جميع المواد</span>
    <h1>قيّم نفسك بنفسك</h1>
    <p class="subtitle">أجب عن الأسئلة بصدق، وفي النهاية بتعرف مستواك وترسله لمعلمك مباشرة.</p>

    <label for="in-name">اسم الطالب</label>
    <input type="text" id="in-name" placeholder="اكتب اسمك الكامل">

    <label for="in-grade">الصف / المرحلة</label>
    <input type="text" id="in-grade" placeholder="مثال: خامس ابتدائي - ب">

    <label for="in-subject">المادة الدراسية</label>
    <input type="text" id="in-subject" placeholder="مثال: اللغة العربية">

    <label for="in-lesson">اسم الدرس</label>
    <input type="text" id="in-lesson" placeholder="مثال: الجملة الاسمية">

    <label>صورة الطالب (اختياري، لتسهيل التعرف عليك)</label>
    <div class="photo-row">
      <div class="photo-frame" id="photo-frame">
        <span class="ph-icon">👤</span>
        <img id="photo-preview" style="display:none;">
      </div>
      <div class="photo-actions">
        <label class="photo-btn" for="in-photo">📷 اختر أو التقط صورة</label>
        <input type="file" id="in-photo" accept="image/*" capture="user">
        <button type="button" class="photo-remove" id="btn-remove-photo">إزالة الصورة</button>
        <p class="hint">تُستخدم الصورة والتاريخ والوقت لتسهيل معرفة هوية الطالب أثناء المراجعة، ولا يتم رفعها لأي خادم خارجي.</p>
      </div>
    </div>

    <button class="btn btn-primary" id="btn-start">ابدأ التقييم</button>

    <div style="text-align:center; margin-top:14px;">
      <a href="#" id="link-teacher-panel" style="font-size:12.5px; color:var(--ink-soft); text-decoration:underline;">لوحة المعلم: إضافة أو تعديل الأسئلة</a>
    </div>
  </div>

  <!-- لوحة المعلم لإدخال الأسئلة يدويًا -->
  <div class="card" id="screen-teacher" style="display:none;">
    <span class="eyebrow">لوحة المعلم</span>
    <h1 style="font-size:24px;">إدارة الأسئلة</h1>
    <p class="subtitle" id="t-mode-note">أضف أسئلتك الخاصة هنا. تُحفظ في هذا المتصفح/الجهاز وتُستخدم تلقائيًا بدل البنك الافتراضي عند وجودها.</p>

    <label>المادة الدراسية</label>
    <input type="text" id="t-subject" placeholder="مثال: اللغة العربية">
    <label>الصف / المرحلة</label>
    <input type="text" id="t-grade" placeholder="مثال: خامس ابتدائي - ب">
    <label>اسم الدرس</label>
    <input type="text" id="t-lesson" placeholder="مثال: الجملة الاسمية">

    <label>صورة أو خريطة مرفقة بالسؤال (اختياري)</label>
    <div class="photo-row" style="align-items:flex-start;">
      <div class="photo-frame" id="q-photo-frame" style="border-radius:12px; width:90px; height:90px;">
        <span class="ph-icon">🖼️</span>
        <img id="q-photo-preview" style="display:none;">
      </div>
      <div class="photo-actions">
        <label class="photo-btn" for="t-image-file" id="t-image-file-label">📎 ارفع صورة من الجهاز</label>
        <input type="file" id="t-image-file" accept="image/*">
        <button type="button" class="photo-remove" id="btn-remove-q-photo">إزالة الصورة</button>
        <p class="hint" id="t-image-hint">تُعرض هذه الصورة للطالب فوق نص هذا السؤال فقط (مثال: خريطة، رسم توضيحي، مستند).</p>
        <label style="margin-top:10px;">أو رابط صورة/خريطة من الإنترنت (اختياري)</label>
        <input type="text" id="t-image-url" placeholder="https://...">
      </div>
    </div>

    <label>نوع السؤال</label>
    <select id="t-type" style="width:100%; padding:12px; border-radius:11px; border:1.5px solid var(--line); font-family:'Tajawal',sans-serif; font-size:15px;">
      <option value="mcq">اختيار من متعدد</option>
      <option value="tf">صح أم خطأ</option>
    </select>

    <label>نص السؤال</label>
    <input type="text" id="t-text" placeholder="اكتب نص السؤال هنا">

    <div id="t-mcq-fields">
      <label>الخيار 1</label>
      <input type="text" id="t-opt1" placeholder="الخيار الأول">
      <label>الخيار 2</label>
      <input type="text" id="t-opt2" placeholder="الخيار الثاني">
      <label>الخيار 3</label>
      <input type="text" id="t-opt3" placeholder="الخيار الثالث">
      <label>الخيار 4</label>
      <input type="text" id="t-opt4" placeholder="الخيار الرابع">
      <label>رقم الخيار الصحيح (1-4)</label>
      <input type="text" id="t-correct-idx" placeholder="مثال: 2">
    </div>

    <div id="t-tf-fields" style="display:none;">
      <label>الإجابة الصحيحة</label>
      <select id="t-correct-tf" style="width:100%; padding:12px; border-radius:11px; border:1.5px solid var(--line); font-family:'Tajawal',sans-serif; font-size:15px;">
        <option value="true">صح</option>
        <option value="false">خطأ</option>
      </select>
    </div>

    <button class="btn btn-primary" id="btn-add-question">إضافة السؤال إلى البنك</button>
    <p id="t-error" style="color:#b23a3a; font-size:13px; display:none; margin-top:8px;"></p>

    <div class="breakdown" id="t-list" style="max-height:260px; margin-top:22px;"></div>

    <div style="display:flex; gap:10px; margin-top:18px;">
      <button class="btn btn-ghost" id="btn-clear-questions" style="flex:1;">حذف كل الأسئلة المضافة</button>
      <button class="btn btn-ghost" id="btn-back-start" style="flex:1;">رجوع</button>
    </div>
  </div>

  <!-- شاشة الأسئلة -->
  <div class="card" id="screen-quiz" style="display:none;">
    <div class="student-badge" id="quiz-student-badge"></div>
    <div class="book-progress">
      <svg width="34" height="26" viewBox="0 0 34 26" fill="none">
        <path d="M17 4 C13 1 6 1 2 3 V22 C6 20 13 20 17 23 C21 20 28 20 32 22 V3 C28 1 21 1 17 4 Z"
          stroke="#6b4a73" stroke-width="2" fill="rgba(107,74,115,0.08)"/>
        <line x1="17" y1="4" x2="17" y2="23" stroke="#6b4a73" stroke-width="1.5"/>
      </svg>
      <span class="folio-label" id="folio-label">سؤال ١ من ١٠</span>
      <div class="folio-track"><div class="folio-fill" id="folio-fill"></div></div>
    </div>
    <span class="q-type" id="q-type-badge">اختيار من متعدد</span>
    <div id="q-image-wrap" style="display:none;"></div>
    <div class="q-text" id="q-text"></div>
    <div class="options" id="q-options"></div>

    <div class="nav-row">
      <button class="btn btn-ghost" id="btn-prev">السابق</button>
      <button class="btn btn-primary btn-next" id="btn-next" style="width:auto; margin-top:0;" disabled>التالي</button>
    </div>
  </div>

  <!-- شاشة النتيجة -->
  <div class="card" id="screen-result" style="display:none;">
    <div class="result-wrap">
      <span class="eyebrow">النتيجة النهائية</span>
      <div class="student-badge" id="result-student-badge" style="text-align:right;"></div>
      <svg class="medal" id="medal-svg" viewBox="0 0 150 170">
        <g id="medal-ribbon">
          <path d="M60 70 L40 160 L75 145 L110 160 L90 70 Z" fill="#6b4a73"/>
        </g>
        <circle cx="75" cy="60" r="52" fill="#fff" stroke="#de8b3b" stroke-width="6"/>
        <circle cx="75" cy="60" r="40" fill="none" stroke="#1e6e76" stroke-width="3" stroke-dasharray="4 5"/>
        <text id="medal-percent" x="75" y="68" text-anchor="middle" font-family="Reem Kufi, sans-serif" font-size="26" font-weight="700" fill="#2a2420">0%</text>
      </svg>

      <div class="level-name" id="level-name">—</div>
      <div class="score-line" id="score-text"></div>
      <div class="timestamp-line" id="timestamp-line"></div>

      <div class="breakdown" id="breakdown"></div>

      <div class="send-box">
        <div class="send-title">إرسال النتيجة إلى المعلم</div>
        <label for="in-teacher-email">البريد الإلكتروني للمعلم</label>
        <input type="email" id="in-teacher-email" placeholder="example@school.com">
        <button class="btn btn-primary" id="btn-send">إرسال النتيجة الآن</button>
        <p class="status-msg status-ok" id="ok-msg">تم إرسال النتيجة إلى معلمك بنجاح ✅</p>
        <p class="status-msg status-err" id="err-msg">تعذّر الإرسال المباشر، جرّب مرة أخرى أو استخدم زر النسخ ⬇️</p>
        <p class="status-msg status-err" id="err-detail" style="font-size:12px; font-weight:400; opacity:0.85;"></p>
        <button class="btn btn-ghost" id="btn-copy" style="width:100%; margin-top:10px;">نسخ النتيجة كنص احتياطي</button>
        <p class="hint status-msg status-ok" id="copy-msg" style="text-align:center;">تم نسخ النتيجة، الصقها بأي وسيلة تواصل ✅</p>
      </div>

      <button class="btn btn-ghost" id="btn-restart" style="width:100%; margin-top:14px;">إعادة المحاولة</button>
    </div>
  </div>

  <p class="footer-note">مدرسة الموالح الخاصة · سلطنة عُمان</p>
  <p class="footer-note" style="margin-top:2px;">تطوير: ا/خالد محمد عبد العظيم — معلم لغة عربية · <a href="mailto:adhamk986@gmail.com" style="color:inherit; text-decoration:underline;">adhamk986@gmail.com</a></p>
</div>

<script>
/* ====================================================================
   إعدادات المعلم — عدّل هنا فقط
   ==================================================================== */

const EMAILJS_PUBLIC_KEY  = "CY0DMJnP6_riOqljt";
const EMAILJS_SERVICE_ID  = "service_hf5e4i2";
const EMAILJS_TEMPLATE_ID = "template_y23rpya";

const GOOGLE_SHEET_CSV_URL = "";
const GOOGLE_SCRIPT_URL = "";

const FALLBACK_QUESTIONS = [
  { type: "mcq", text: "عمل «لا» النافية للجنس يشبه عمل:",
    options: ["إنّ وأخواتها", "كان وأخواتها", "ظنّ وأخواتها", "حروف الجر"], correctIndex: 0 },
  { type: "tf", text: "«لا» النافية للجنس ترفع الاسم وتنصب الخبر.", correct: false },
  { type: "mcq", text: "في جملة «لا رجلَ في الدار» إعراب «رجلَ»:",
    options: ["اسم لا مبني على الفتح في محل نصب", "اسم لا مضاف منصوب", "خبر لا مرفوع", "مبتدأ مرفوع"], correctIndex: 0 },
  { type: "mcq", text: "في جملة «لا طالبَ علمٍ مهملٌ» إعراب «طالبَ»:",
    options: ["اسم لا مبني على الفتح", "اسم لا منصوب لأنه مضاف", "خبر لا مرفوع", "فاعل مرفوع"], correctIndex: 1 },
  { type: "tf", text: "من شروط عمل «لا» النافية للجنس ألا يُفصل بينها وبين اسمها بفاصل.", correct: true },
  { type: "mcq", text: "خبر «لا» النافية للجنس إذا كان معلومًا من السياق غالبًا:",
    options: ["يُذكر وجوبًا", "يُحذف", "يُنصب", "يُجزم"], correctIndex: 1 },
  { type: "mcq", text: "أي مما يلي اسم «لا» فيه «شبيه بالمضاف»؟",
    options: ["لا معلمَ في المدرسة", "لا طالبَ علمٍ كسولٌ", "لا مهملًا واجبَه محمودٌ", "لا كتابَ مفيدٌ"], correctIndex: 2 },
  { type: "tf", text: "يُشترط في اسم وخبر «لا» النافية للجنس أن يكونا معرفتين.", correct: false },
  { type: "mcq", text: "النفي في «لا إلهَ إلا الله» يفيد:",
    options: ["نفيًا مؤقتًا", "نفي الجنس على سبيل الاستغراق والشمول", "نفيًا جزئيًا", "إثباتًا"], correctIndex: 1 },
  { type: "mcq", text: "إذا تكررت «لا» النافية للجنس في الجملة، يجوز فيها:",
    options: ["الإعمال فقط", "الإهمال فقط", "الإعمال أو الإهمال", "لا شيء مما ذكر"], correctIndex: 2 },
  { type: "tf", text: "اسم «لا» النافية للجنس إذا كان مضافًا يُبنى على ما يُنصب به.", correct: false },
  { type: "mcq", text: "في جملة «لا كسولَينِ في الفصل» نوع اسم «لا»:",
    options: ["مفرد مبني", "مثنى أو جمع معرب", "مضاف", "شبيه بالمضاف"], correctIndex: 1 }
];

let QUESTIONS = FALLBACK_QUESTIONS;
let current = 0;
let answers = [];
let studentInfo = {};
let studentPhotoData = null;

function resizeImageToDataURL(file, maxDim, quality){
  return new Promise((resolve, reject) => {
    const reader = new FileReader();
    reader.onload = (e) => {
      const img = new Image();
      img.onload = () => {
        let { width, height } = img;
        if(width > height){
          if(width > maxDim){ height = Math.round(height * maxDim / width); width = maxDim; }
        } else {
          if(height > maxDim){ width = Math.round(width * maxDim / height); height = maxDim; }
        }
        const canvas = document.createElement('canvas');
        canvas.width = width; canvas.height = height;
        const ctx = canvas.getContext('2d');
        ctx.drawImage(img, 0, 0, width, height);
        resolve(canvas.toDataURL('image/jpeg', quality));
      };
      img.onerror = reject;
      img.src = e.target.result;
    };
    reader.onerror = reject;
    reader.readAsDataURL(file);
  });
}

const photoInput = document.getElementById('in-photo');
const photoPreview = document.getElementById('photo-preview');
const photoFrameIcon = document.querySelector('#photo-frame .ph-icon');
const btnRemovePhoto = document.getElementById('btn-remove-photo');

photoInput.addEventListener('change', async () => {
  const file = photoInput.files && photoInput.files[0];
  if(!file) return;
  try{
    studentPhotoData = await resizeImageToDataURL(file, 220, 0.6);
    photoPreview.src = studentPhotoData;
    photoPreview.style.display = 'block';
    photoFrameIcon.style.display = 'none';
    btnRemovePhoto.style.display = 'inline';
  } catch(e){
    console.warn('تعذّرت معالجة صورة الطالب', e);
  }
});

btnRemovePhoto.addEventListener('click', () => {
  studentPhotoData = null;
  photoInput.value = '';
  photoPreview.src = '';
  photoPreview.style.display = 'none';
  photoFrameIcon.style.display = 'block';
  btnRemovePhoto.style.display = 'none';
});

const ARABIC_MONTHS = ["يناير","فبراير","مارس","أبريل","مايو","يونيو","يوليو","أغسطس","سبتمبر","أكتوبر","نوفمبر","ديسمبر"];

function getAcademicYear(d){
  const y = d.getFullYear();
  const m = d.getMonth();
  return m >= 8 ? `${y}/${y+1}` : `${y-1}/${y}`;
}

function formatArabicDateTime(d){
  const day = toArabicDigits(d.getDate());
  const month = ARABIC_MONTHS[d.getMonth()];
  const year = toArabicDigits(d.getFullYear());
  let hours = d.getHours();
  const minutes = toArabicDigits(String(d.getMinutes()).padStart(2,'0'));
  const period = hours >= 12 ? 'م' : 'ص';
  hours = hours % 12; if(hours === 0) hours = 12;
  return {
    dateStr: `${day} ${month} ${year}`,
    timeStr: `${toArabicDigits(hours)}:${minutes} ${period}`
  };
}

function renderStudentBadge(containerId){
  const el = document.getElementById(containerId);
  if(!el) return;
  const photoHtml = studentPhotoData
    ? `<img src="${studentPhotoData}" alt="صورة الطالب">`
    : `<div class="sb-icon">${(studentInfo.name || '؟').trim().charAt(0)}</div>`;
  el.innerHTML = `
    ${photoHtml}
    <div class="sb-info">
      <div class="sb-name">${studentInfo.name}</div>
      <div class="sb-meta">${studentInfo.grade} · ${studentInfo.subject}</div>
    </div>
  `;
}

function parseCSVLine(line){
  const result = [];
  let cur = '';
  let inQuotes = false;
  for(let i = 0; i < line.length; i++){
    const ch = line[i];
    if(inQuotes){
      if(ch === '"'){
        if(line[i+1] === '"'){ cur += '"'; i++; }
        else { inQuotes = false; }
      } else { cur += ch; }
    } else {
      if(ch === '"'){ inQuotes = true; }
      else if(ch === ','){ result.push(cur); cur = ''; }
      else { cur += ch; }
    }
  }
  result.push(cur);
  return result;
}

function parseCSV(text){
  const lines = text.split(/\r\n|\n/).filter(l => l.trim().length > 0);
  return lines.map(parseCSVLine);
}

function norm(s){
  return (s || '').toString().trim().toLowerCase();
}

async function fetchSheetQuestions(subject, grade, lesson){
  if(!GOOGLE_SHEET_CSV_URL) return [];
  try{
    const res = await fetch(GOOGLE_SHEET_CSV_URL, { cache: "no-store" });
    if(!res.ok) throw new Error("fetch failed");
    const text = await res.text();
    const rows = parseCSV(text);
    if(rows.length < 2) return [];
    const dataRows = rows.slice(1);
    const parsed = dataRows.map(cols => {
      const [rSubject, rGrade, rLesson, rType, rText, o1, o2, o3, o4, rAnswer, rImage] = cols;
      const type = norm(rType) === 'tf' ? 'tf' : 'mcq';
      const image = (rImage || '').trim() || undefined;
      if(type === 'tf'){
        return {
          subject: rSubject, grade: rGrade, lesson: rLesson,
          type: 'tf',
          text: (rText || '').trim(),
          correct: norm(rAnswer) === 'صح' || norm(rAnswer) === 'true',
          image
        };
      }
      const options = [o1, o2, o3, o4].map(o => (o || '').trim());
      let idx = parseInt(rAnswer, 10);
      if(isNaN(idx) || idx < 1 || idx > 4) idx = 1;
      return {
        subject: rSubject, grade: rGrade, lesson: rLesson,
        type: 'mcq',
        text: (rText || '').trim(),
        options,
        correctIndex: idx - 1,
        image
      };
    }).filter(q => q.text);

    const bySubjectGradeLesson = parsed.filter(q =>
      norm(q.subject) === norm(subject) && norm(q.grade) === norm(grade) &&
      lesson && norm(q.lesson) === norm(lesson));
    if(bySubjectGradeLesson.length) return bySubjectGradeLesson;

    const bySubjectGrade = parsed.filter(q =>
      norm(q.subject) === norm(subject) && norm(q.grade) === norm(grade));
    if(bySubjectGrade.length) return bySubjectGrade;

    const bySubject = parsed.filter(q => norm(q.subject) === norm(subject));
    if(bySubject.length) return bySubject;

    return [];
  } catch(e){
    console.warn("تعذّر تحميل الأسئلة من الشيت، سيتم استخدام البنك الاحتياطي.", e);
    return [];
  }
}

const screenStart = document.getElementById('screen-start');
const screenQuiz = document.getElementById('screen-quiz');
const screenResult = document.getElementById('screen-result');
const screenTeacher = document.getElementById('screen-teacher');

const CUSTOM_KEY = 'qnf_custom_questions';

function loadCustomQuestions(){
  try{
    const raw = localStorage.getItem(CUSTOM_KEY);
    return raw ? JSON.parse(raw) : [];
  } catch(e){ return []; }
}

function saveCustomQuestions(list){
  try{ localStorage.setItem(CUSTOM_KEY, JSON.stringify(list)); } catch(e){}
}

function renderTeacherList(){
  if(GOOGLE_SCRIPT_URL){
    const wrap = document.getElementById('t-list');
    wrap.innerHTML = '<div style="text-align:center; color:var(--ink-soft); font-size:13px;">الأسئلة تُرسل مباشرة إلى الشيت المشترك — راجعها من هناك.</div>';
    return;
  }
  const list = loadCustomQuestions();
  const wrap = document.getElementById('t-list');
  if(!list.length){
    wrap.innerHTML = '<div style="text-align:center; color:var(--ink-soft); font-size:13px;">لا توجد أسئلة مضافة بعد.</div>';
    return;
  }
  wrap.innerHTML = list.map((q, i) => `
    <div class="breakdown-item">
      <span>${i+1}. ${q.text} (${q.type === 'mcq' ? 'اختيار' : 'صح/خطأ'})${q.image ? ' 🖼️' : ''}</span>
      <span><a href="#" data-idx="${i}" class="del-question" style="color:#b23a3a; font-weight:800; text-decoration:none;">حذف ✕</a></span>
    </div>
  `).join('');
  wrap.querySelectorAll('.del-question').forEach(a => {
    a.addEventListener('click', (e) => {
      e.preventDefault();
      const idx = parseInt(a.getAttribute('data-idx'), 10);
      const l = loadCustomQuestions();
      l.splice(idx, 1);
      saveCustomQuestions(l);
      renderTeacherList();
    });
  });
}

document.getElementById('link-teacher-panel').addEventListener('click', (e) => {
  e.preventDefault();
  screenStart.style.display = 'none';
  screenTeacher.style.display = 'block';
  renderTeacherList();
});

document.getElementById('btn-back-start').addEventListener('click', () => {
  screenTeacher.style.display = 'none';
  screenStart.style.display = 'block';
});

document.getElementById('t-type').addEventListener('change', (e) => {
  const isMcq = e.target.value === 'mcq';
  document.getElementById('t-mcq-fields').style.display = isMcq ? 'block' : 'none';
  document.getElementById('t-tf-fields').style.display = isMcq ? 'none' : 'block';
});

let questionImageData = null;
const qImageFileInput = document.getElementById('t-image-file');
const qImageFileLabel = document.getElementById('t-image-file-label');
const qImageHint = document.getElementById('t-image-hint');
const qImageUrlInput = document.getElementById('t-image-url');
const qPhotoPreview = document.getElementById('q-photo-preview');
const qPhotoFrameIcon = document.querySelector('#q-photo-frame .ph-icon');
const btnRemoveQPhoto = document.getElementById('btn-remove-q-photo');

function resetQuestionImageField(){
  questionImageData = null;
  qImageFileInput.value = '';
  qImageUrlInput.value = '';
  qPhotoPreview.src = '';
  qPhotoPreview.style.display = 'none';
  qPhotoFrameIcon.style.display = 'block';
  btnRemoveQPhoto.style.display = 'none';
}

qImageFileInput.addEventListener('change', async () => {
  const file = qImageFileInput.files && qImageFileInput.files[0];
  if(!file) return;
  try{
    questionImageData = await resizeImageToDataURL(file, 720, 0.7);
    qPhotoPreview.src = questionImageData;
    qPhotoPreview.style.display = 'block';
    qPhotoFrameIcon.style.display = 'none';
    btnRemoveQPhoto.style.display = 'inline';
  } catch(e){
    console.warn('تعذّرت معالجة صورة السؤال', e);
  }
});

btnRemoveQPhoto.addEventListener('click', resetQuestionImageField);

if(GOOGLE_SCRIPT_URL){
  qImageFileLabel.style.display = 'none';
  qImageFileInput.style.display = 'none';
  qImageHint.textContent = 'في وضع البنك المشترك أضف رابط صورة (مثل رابط مشاركة عامة من Google Drive أو أي استضافة صور) بدل الرفع المباشر.';
}

if(GOOGLE_SCRIPT_URL){
  const noteEl = document.getElementById('t-mode-note');
  if(noteEl) noteEl.textContent = 'الأسئلة هنا تُرسل إلى بنك الأسئلة المشترك (Google Sheet) ويستفيد منها كل المعلمين والطلاب فورًا.';
}

async function sendQuestionToSheet(payload){
  const res = await fetch(GOOGLE_SCRIPT_URL, {
    method: 'POST',
    headers: { 'Content-Type': 'text/plain;charset=utf-8' },
    body: JSON.stringify(payload)
  });
  if(!res.ok) throw new Error('HTTP ' + res.status);
}

document.getElementById('btn-add-question').addEventListener('click', async () => {
  const errEl = document.getElementById('t-error');
  errEl.style.display = 'none';
  const type = document.getElementById('t-type').value;
  const text = document.getElementById('t-text').value.trim();
  const subject = document.getElementById('t-subject').value.trim();
  const grade = document.getElementById('t-grade').value.trim();
  const lesson = document.getElementById('t-lesson').value.trim();

  if(!text){ errEl.textContent = 'اكتب نص السؤال أولًا.'; errEl.style.display = 'block'; return; }
  if(GOOGLE_SCRIPT_URL && (!subject || !grade)){
    errEl.textContent = 'اكتب المادة والصف على الأقل حتى يصل السؤال للطلاب الصحيحين.';
    errEl.style.display = 'block';
    return;
  }

  const imageUrl = qImageUrlInput.value.trim();
  const image = questionImageData || imageUrl || null;

  let q, sheetRow;
  if(type === 'mcq'){
    const options = [1,2,3,4].map(n => document.getElementById('t-opt'+n).value.trim());
    if(options.some(o => !o)){ errEl.textContent = 'اكتب كل الخيارات الأربعة.'; errEl.style.display = 'block'; return; }
    let idx = parseInt(document.getElementById('t-correct-idx').value, 10);
    if(isNaN(idx) || idx < 1 || idx > 4){ errEl.textContent = 'رقم الخيار الصحيح يجب أن يكون من 1 إلى 4.'; errEl.style.display = 'block'; return; }
    q = { type: 'mcq', text, options, correctIndex: idx - 1 };
    if(image) q.image = image;
    sheetRow = { subject, grade, lesson, type: 'mcq', text, o1: options[0], o2: options[1], o3: options[2], o4: options[3], answer: idx, image: imageUrl };
  } else {
    const correct = document.getElementById('t-correct-tf').value === 'true';
    q = { type: 'tf', text, correct };
    if(image) q.image = image;
    sheetRow = { subject, grade, lesson, type: 'tf', text, o1: '', o2: '', o3: '', o4: '', answer: correct ? 'صح' : 'خطأ', image: imageUrl };
  }

  const addBtn = document.getElementById('btn-add-question');
  const originalLabel = addBtn.textContent;

  if(GOOGLE_SCRIPT_URL){
    addBtn.disabled = true;
    addBtn.textContent = 'جاري الإرسال...';
    try{
      await sendQuestionToSheet(sheetRow);
    } catch(e){
      errEl.textContent = 'تعذّر الإرسال إلى الشيت المشترك، تحقق من الاتصال أو من إعداد GOOGLE_SCRIPT_URL.';
      errEl.style.display = 'block';
      addBtn.disabled = false;
      addBtn.textContent = originalLabel;
      return;
    }
    addBtn.disabled = false;
    addBtn.textContent = originalLabel;
  } else {
    const list = loadCustomQuestions();
    list.push(q);
    saveCustomQuestions(list);
  }

  document.getElementById('t-text').value = '';
  [1,2,3,4].forEach(n => document.getElementById('t-opt'+n).value = '');
  document.getElementById('t-correct-idx').value = '';
  resetQuestionImageField();
  renderTeacherList();
});

document.getElementById('btn-clear-questions').addEventListener('click', () => {
  if(!confirm('هل أنت متأكد من حذف كل الأسئلة المضافة؟ سيتم الرجوع للبنك الافتراضي.')) return;
  saveCustomQuestions([]);
  renderTeacherList();
});

document.getElementById('btn-start').addEventListener('click', async () => {
  const name = document.getElementById('in-name').value.trim();
  const grade = document.getElementById('in-grade').value.trim();
  const subject = document.getElementById('in-subject').value.trim();
  const lesson = document.getElementById('in-lesson').value.trim();
  if(!name){ document.getElementById('in-name').focus(); return; }
  const startMoment = new Date();
  const { dateStr, timeStr } = formatArabicDateTime(startMoment);
  studentInfo = {
    name,
    grade: grade || "غير محدد",
    subject: subject || "غير محدد",
    lesson: lesson || "غير محدد",
    date: dateStr,
    time: timeStr,
    academicYear: getAcademicYear(startMoment)
  };

  const startBtn = document.getElementById('btn-start');
  const originalLabel = startBtn.textContent;
  startBtn.disabled = true;
  startBtn.textContent = 'جاري تحضير الأسئلة...';

  const customQuestions = loadCustomQuestions();
  if(customQuestions.length){
    QUESTIONS = customQuestions;
  } else {
    let sheetQuestions = [];
    if(GOOGLE_SHEET_CSV_URL){
      sheetQuestions = await fetchSheetQuestions(subject, grade, lesson);
    }
    QUESTIONS = sheetQuestions.length ? sheetQuestions : FALLBACK_QUESTIONS;
  }

  startBtn.disabled = false;
  startBtn.textContent = originalLabel;

  current = 0;
  answers = new Array(QUESTIONS.length).fill(null);

  screenStart.style.display = 'none';
  screenQuiz.style.display = 'block';
  renderStudentBadge('quiz-student-badge');
  renderQuestion();
});

function toArabicDigits(n){
  const map = ['٠','١','٢','٣','٤','٥','٦','٧','٨','٩'];
  return String(n).split('').map(d => map[+d] ?? d).join('');
}

function renderQuestion(){
  const q = QUESTIONS[current];
  document.getElementById('folio-label').textContent =
    `سؤال ${toArabicDigits(current+1)} من ${toArabicDigits(QUESTIONS.length)}`;
  document.getElementById('folio-fill').style.width = ((current)/QUESTIONS.length*100) + "%";
  document.getElementById('q-type-badge').textContent = q.type === 'mcq' ? 'اختيار من متعدد' : 'صح أم خطأ';

  const qImageWrap = document.getElementById('q-image-wrap');
  if(q.image){
    qImageWrap.innerHTML = `<a href="${q.image}" target="_blank" rel="noopener"><img src="${q.image}" alt="صورة توضيحية للسؤال" style="width:100%; border-radius:14px; margin:4px 0 18px; display:block; border:1.5px solid var(--line);"></a>`;
    qImageWrap.style.display = 'block';
  } else {
    qImageWrap.innerHTML = '';
    qImageWrap.style.display = 'none';
  }

  document.getElementById('q-text').textContent = q.text;

  const optsWrap = document.getElementById('q-options');
  optsWrap.innerHTML = '';

  if(q.type === 'mcq'){
    optsWrap.className = 'options';
    q.options.forEach((opt, idx) => {
      const div = document.createElement('div');
      div.className = 'opt' + (answers[current] === idx ? ' selected' : '');
      div.textContent = opt;
      div.addEventListener('click', () => selectAnswer(idx));
      optsWrap.appendChild(div);
    });
  } else {
    optsWrap.className = 'options tf-row';
    const trueDiv = document.createElement('div');
    trueDiv.className = 'opt' + (answers[current] === true ? ' selected' : '');
    trueDiv.textContent = 'صح';
    trueDiv.addEventListener('click', () => selectAnswer(true));
    const falseDiv = document.createElement('div');
    falseDiv.className = 'opt' + (answers[current] === false ? ' selected' : '');
    falseDiv.textContent = 'خطأ';
    falseDiv.addEventListener('click', () => selectAnswer(false));
    optsWrap.appendChild(trueDiv);
    optsWrap.appendChild(falseDiv);
  }

  document.getElementById('btn-prev').style.visibility = current === 0 ? 'hidden' : 'visible';
  document.getElementById('btn-next').disabled = answers[current] === null;
  document.getElementById('btn-next').textContent =
    current === QUESTIONS.length - 1 ? 'إنهاء وعرض النتيجة' : 'التالي';
}

function selectAnswer(val){ answers[current] = val; renderQuestion(); }

document.getElementById('btn-prev').addEventListener('click', () => {
  if(current > 0){ current--; renderQuestion(); }
});

document.getElementById('btn-next').addEventListener('click', () => {
  if(answers[current] === null) return;
  if(current < QUESTIONS.length - 1){ current++; renderQuestion(); }
  else { showResult(); }
});

function showResult(){
  let correctCount = 0;
  const details = QUESTIONS.map((q, i) => {
    let isCorrect = q.type === 'mcq' ? answers[i] === q.correctIndex : answers[i] === q.correct;
    if(isCorrect) correctCount++;
    return { text: q.text, isCorrect };
  });

  const total = QUESTIONS.length;
  const percent = Math.round((correctCount / total) * 100);

  let level, levelClass, ribbonColor;
  if(percent >= 90){ level = 'ممتاز'; levelClass = 'lvl-teal'; ribbonColor = '#1e6e76'; }
  else if(percent >= 75){ level = 'جيد جدًا'; levelClass = 'lvl-olive'; ribbonColor = '#8fa23e'; }
  else if(percent >= 60){ level = 'جيد'; levelClass = 'lvl-orange'; ribbonColor = '#de8b3b'; }
  else { level = 'يحتاج إلى تحسين'; levelClass = 'lvl-plum'; ribbonColor = '#6b4a73'; }

  screenQuiz.style.display = 'none';
  screenResult.style.display = 'block';

  const levelEl = document.getElementById('level-name');
  levelEl.textContent = level;
  levelEl.className = 'level-name ' + levelClass;

  document.getElementById('score-text').textContent =
    `${studentInfo.name} حصل/ت على ${correctCount} من ${total} إجابة صحيحة`;
  document.getElementById('timestamp-line').textContent =
    `📅 ${studentInfo.date} · 🕒 ${studentInfo.time} · العام الدراسي ${studentInfo.academicYear}`;
  renderStudentBadge('result-student-badge');

  document.getElementById('medal-percent').textContent = percent + '%';
  document.getElementById('medal-ribbon').querySelector('path').setAttribute('fill', ribbonColor);

  const breakdown = document.getElementById('breakdown');
  breakdown.innerHTML = details.map((d, i) =>
    `<div class="breakdown-item"><span>س${toArabicDigits(i+1)}: ${d.text}</span>
     <span class="${d.isCorrect ? 'tag-ok' : 'tag-no'}">${d.isCorrect ? '✓ صحيح' : '✗ خطأ'}</span></div>`
  ).join('');

  window._resultData = { correctCount, total, percent, level, details };
}

function buildResultText(){
  const { correctCount, total, percent, level, details } = window._resultData;
  let body = `نتيجة تقييم ذاتي - ${studentInfo.subject}\n`;
  body += `الاسم: ${studentInfo.name}\nالصف: ${studentInfo.grade}\nالمادة: ${studentInfo.subject}\nالدرس: ${studentInfo.lesson}\n`;
  body += `التاريخ: ${studentInfo.date}\nالوقت: ${studentInfo.time}\nالعام الدراسي: ${studentInfo.academicYear}\n`;
  body += `النتيجة: ${correctCount} من ${total} (${percent}٪)\nالمستوى: ${level}\n\nتفاصيل الإجابات:\n`;
  details.forEach((d, i) => { body += `${i+1}. ${d.text} — ${d.isCorrect ? 'صحيح' : 'خطأ'}\n`; });
  return body;
}

document.getElementById('btn-send').addEventListener('click', async () => {
  const teacherEmail = document.getElementById('in-teacher-email').value.trim();
  const okMsg = document.getElementById('ok-msg');
  const errMsg = document.getElementById('err-msg');
  okMsg.style.display = 'none';
  errMsg.style.display = 'none';
  document.getElementById('err-detail').style.display = 'none';

  if(!teacherEmail || !teacherEmail.includes('@')){
    document.getElementById('in-teacher-email').focus();
    return;
  }

  const { correctCount, total, percent, level } = window._resultData;
  const btn = document.getElementById('btn-send');
  btn.disabled = true;
  btn.textContent = 'جاري الإرسال...';

  const templateParams = {
    to_email: teacherEmail,
    student_name: studentInfo.name,
    grade: studentInfo.grade,
    subject: studentInfo.subject,
    lesson: studentInfo.lesson,
    date: studentInfo.date,
    time: studentInfo.time,
    academic_year: studentInfo.academicYear,
    score: `${correctCount} من ${total}`,
    percent: percent + '%',
    level: level,
    details: buildResultText(),
    student_photo: studentPhotoData || ''
  };

  try{
    if(EMAILJS_PUBLIC_KEY === "YOUR_PUBLIC_KEY"){
      throw new Error("EmailJS not configured");
    }
    const res = await fetch('https://api.emailjs.com/api/v1.0/email/send', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        service_id: EMAILJS_SERVICE_ID,
        template_id: EMAILJS_TEMPLATE_ID,
        user_id: EMAILJS_PUBLIC_KEY,
        template_params: templateParams
      })
    });
    if(!res.ok){
      const bodyText = await res.text().catch(() => '');
      throw new Error(`HTTP ${res.status}: ${bodyText}`);
    }
    okMsg.style.display = 'block';
  } catch(e){
    errMsg.style.display = 'block';
    const detailEl = document.getElementById('err-detail');
    detailEl.textContent = 'تفاصيل الخطأ (للمطور): ' + (e && e.message ? e.message : String(e));
    detailEl.style.display = 'block';
  } finally {
    btn.disabled = false;
    btn.textContent = 'إرسال النتيجة الآن';
  }
});

document.getElementById('btn-copy').addEventListener('click', async () => {
  const teacherEmail = document.getElementById('in-teacher-email').value.trim();
  const text = (teacherEmail ? `إلى: ${teacherEmail}\n\n` : '') + buildResultText();
  try{
    await navigator.clipboard.writeText(text);
  } catch(e){
    const ta = document.createElement('textarea');
    ta.value = text; ta.style.position='fixed'; ta.style.opacity='0';
    document.body.appendChild(ta); ta.select();
    document.execCommand('copy'); document.body.removeChild(ta);
  }
  document.getElementById('copy-msg').style.display = 'block';
});

document.getElementById('btn-restart').addEventListener('click', () => {
  current = 0;
  answers = new Array(QUESTIONS.length).fill(null);
  document.getElementById('ok-msg').style.display = 'none';
  document.getElementById('err-msg').style.display = 'none';
  document.getElementById('err-detail').style.display = 'none';
  document.getElementById('copy-msg').style.display = 'none';
  document.getElementById('in-teacher-email').value = '';
  screenResult.style.display = 'none';
  screenStart.style.display = 'block';
});
</script>
</body>
</html>
