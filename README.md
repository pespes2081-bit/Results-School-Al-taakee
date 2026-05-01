# Results-School-Al-taakee
نتائج اعدادية التاخي للبنين
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>نتائج طلاب اعدادية التآخي للبنين</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #c9a84c;
    --gold-light: #e8c97a;
    --dark: #0d1117;
    --dark2: #161b22;
    --dark3: #21262d;
    --border: #30363d;
    --text: #e6edf3;
    --text-muted: #8b949e;
    --green: #3fb950;
    --red: #f85149;
    --blue: #58a6ff;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Cairo', sans-serif;
    background: var(--dark);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Background pattern */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 20% 20%, rgba(201,168,76,0.07) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 80%, rgba(88,166,255,0.05) 0%, transparent 50%);
    pointer-events: none;
    z-index: 0;
  }

  .page { position: relative; z-index: 1; }

  /* ===== LOGIN PAGE ===== */
  #loginPage {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    padding: 24px;
  }

  .login-card {
    background: var(--dark2);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 48px 40px;
    width: 100%;
    max-width: 440px;
    box-shadow: 0 24px 80px rgba(0,0,0,0.5), 0 0 0 1px rgba(201,168,76,0.1);
    animation: slideUp 0.6s cubic-bezier(0.16,1,0.3,1);
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .school-logo {
    text-align: center;
    margin-bottom: 36px;
  }

  .logo-icon {
    width: 72px;
    height: 72px;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    border-radius: 18px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    margin: 0 auto 16px;
    box-shadow: 0 8px 32px rgba(201,168,76,0.3);
  }

  .school-name {
    font-family: 'Tajawal', sans-serif;
    font-size: 22px;
    font-weight: 800;
    color: var(--gold-light);
    line-height: 1.3;
  }

  .school-sub {
    font-size: 13px;
    color: var(--text-muted);
    margin-top: 6px;
    font-weight: 400;
  }

  .login-title {
    font-size: 28px;
    font-weight: 900;
    text-align: center;
    margin-bottom: 8px;
    background: linear-gradient(135deg, var(--text), var(--gold-light));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .login-subtitle {
    text-align: center;
    color: var(--text-muted);
    font-size: 14px;
    margin-bottom: 32px;
  }

  .field-group {
    margin-bottom: 20px;
  }

  label {
    display: block;
    font-size: 13px;
    font-weight: 600;
    color: var(--text-muted);
    margin-bottom: 8px;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  input[type="text"], input[type="password"] {
    width: 100%;
    background: var(--dark3);
    border: 1.5px solid var(--border);
    border-radius: 12px;
    padding: 14px 18px;
    font-size: 16px;
    font-family: 'Cairo', sans-serif;
    color: var(--text);
    text-align: center;
    letter-spacing: 4px;
    transition: border-color 0.2s, box-shadow 0.2s;
    outline: none;
  }

  input[type="text"]:focus, input[type="password"]:focus {
    border-color: var(--gold);
    box-shadow: 0 0 0 4px rgba(201,168,76,0.15);
  }

  input::placeholder { letter-spacing: 0; color: var(--text-muted); }

  .btn-login {
    width: 100%;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    border: none;
    border-radius: 12px;
    padding: 15px;
    font-size: 16px;
    font-family: 'Cairo', sans-serif;
    font-weight: 700;
    color: var(--dark);
    cursor: pointer;
    margin-top: 8px;
    transition: transform 0.15s, box-shadow 0.15s, opacity 0.15s;
    box-shadow: 0 4px 20px rgba(201,168,76,0.3);
  }

  .btn-login:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(201,168,76,0.4); }
  .btn-login:active { transform: translateY(0); }

  .error-msg {
    background: rgba(248,81,73,0.12);
    border: 1px solid rgba(248,81,73,0.4);
    border-radius: 10px;
    padding: 12px 16px;
    font-size: 14px;
    color: var(--red);
    text-align: center;
    margin-top: 16px;
    display: none;
  }

  .error-msg.show { display: block; animation: shake 0.4s; }

  @keyframes shake {
    0%,100%{transform:translateX(0)} 25%{transform:translateX(-8px)} 75%{transform:translateX(8px)}
  }

  /* ===== ADMIN PAGE ===== */
  #adminPage, #studentPage { display: none; }

  .header {
    background: var(--dark2);
    border-bottom: 1px solid var(--border);
    padding: 0 24px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(10px);
  }

  .header-brand {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .header-icon {
    width: 38px;
    height: 38px;
    background: linear-gradient(135deg, var(--gold), var(--gold-light));
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
  }

  .header-title {
    font-weight: 700;
    font-size: 16px;
    color: var(--gold-light);
  }

  .btn-logout {
    background: var(--dark3);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 8px 16px;
    font-size: 13px;
    font-family: 'Cairo', sans-serif;
    color: var(--text-muted);
    cursor: pointer;
    transition: all 0.2s;
  }

  .btn-logout:hover { border-color: var(--red); color: var(--red); }

  /* ===== ADMIN STUDENTS LIST ===== */
  .admin-content {
    max-width: 1100px;
    margin: 0 auto;
    padding: 32px 24px;
  }

  .admin-stats {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 16px;
    margin-bottom: 32px;
  }

  .stat-card {
    background: var(--dark2);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 20px;
    text-align: center;
  }

  .stat-num {
    font-size: 32px;
    font-weight: 900;
    color: var(--gold-light);
    font-family: 'Tajawal', sans-serif;
  }

  .stat-label {
    font-size: 13px;
    color: var(--text-muted);
    margin-top: 4px;
  }

  .section-title {
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .students-table {
    background: var(--dark2);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
  }

  .students-table table {
    width: 100%;
    border-collapse: collapse;
  }

  .students-table th {
    background: var(--dark3);
    padding: 14px 18px;
    font-size: 13px;
    font-weight: 600;
    color: var(--text-muted);
    text-align: right;
    border-bottom: 1px solid var(--border);
    white-space: nowrap;
  }

  .students-table td {
    padding: 14px 18px;
    font-size: 14px;
    border-bottom: 1px solid rgba(48,54,61,0.6);
    vertical-align: middle;
  }

  .students-table tr:last-child td { border-bottom: none; }

  .students-table tr:hover td { background: rgba(201,168,76,0.04); }

  .pin-badge {
    font-family: 'Courier New', monospace;
    background: var(--dark3);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 4px 10px;
    font-size: 14px;
    letter-spacing: 3px;
    color: var(--gold-light);
    font-weight: 700;
  }

  .view-btn {
    background: rgba(88,166,255,0.1);
    border: 1px solid rgba(88,166,255,0.3);
    border-radius: 8px;
    padding: 6px 14px;
    font-size: 12px;
    font-family: 'Cairo', sans-serif;
    color: var(--blue);
    cursor: pointer;
    transition: all 0.2s;
  }

  .view-btn:hover { background: rgba(88,166,255,0.2); }

  /* ===== STUDENT RESULT PAGE ===== */
  .student-content {
    max-width: 860px;
    margin: 0 auto;
    padding: 32px 24px;
  }

  .result-header {
    background: linear-gradient(135deg, var(--dark2), var(--dark3));
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 32px;
    margin-bottom: 24px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .result-header::before {
    content: '';
    position: absolute;
    top: -40px;
    right: -40px;
    width: 180px;
    height: 180px;
    background: radial-gradient(circle, rgba(201,168,76,0.12) 0%, transparent 70%);
    border-radius: 50%;
  }

  .student-name-display {
    font-family: 'Tajawal', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: var(--gold-light);
    margin-bottom: 8px;
  }

  .student-meta {
    font-size: 14px;
    color: var(--text-muted);
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .meta-badge {
    background: var(--dark3);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 5px 14px;
    font-size: 13px;
  }

  .grades-card {
    background: var(--dark2);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    margin-bottom: 24px;
  }

  .grades-header {
    background: var(--dark3);
    padding: 16px 24px;
    display: flex;
    align-items: center;
    gap: 8px;
    border-bottom: 1px solid var(--border);
    font-weight: 700;
    font-size: 15px;
  }

  .grades-table {
    width: 100%;
    border-collapse: collapse;
  }

  .grades-table th {
    background: rgba(201,168,76,0.08);
    padding: 12px 20px;
    font-size: 13px;
    font-weight: 600;
    color: var(--gold-light);
    text-align: right;
    border-bottom: 1px solid var(--border);
  }

  .grades-table td {
    padding: 13px 20px;
    font-size: 15px;
    border-bottom: 1px solid rgba(48,54,61,0.5);
  }

  .grades-table tr:last-child td { border-bottom: none; }
  .grades-table tr:hover td { background: rgba(255,255,255,0.02); }

  .subject-name {
    font-weight: 600;
    color: var(--text);
  }

  .grade-num {
    font-weight: 700;
    text-align: center;
    font-size: 16px;
  }

  .grade-high { color: var(--green); }
  .grade-mid { color: #d29922; }
  .grade-low { color: var(--red); }

  .grade-bar-wrap {
    width: 120px;
    height: 6px;
    background: var(--dark3);
    border-radius: 4px;
    overflow: hidden;
    display: inline-block;
    vertical-align: middle;
    margin-right: 8px;
  }

  .grade-bar {
    height: 100%;
    border-radius: 4px;
    transition: width 1s ease;
  }

  .academic-year-badge {
    display: inline-block;
    background: linear-gradient(135deg, rgba(201,168,76,0.2), rgba(201,168,76,0.08));
    border: 1px solid rgba(201,168,76,0.4);
    border-radius: 8px;
    padding: 6px 16px;
    font-size: 13px;
    color: var(--gold-light);
    margin-bottom: 16px;
    font-weight: 600;
  }

  .footer-note {
    text-align: center;
    color: var(--text-muted);
    font-size: 13px;
    padding: 16px;
    border-top: 1px solid var(--border);
  }

  .search-box {
    background: var(--dark3);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 10px 16px;
    font-size: 14px;
    font-family: 'Cairo', sans-serif;
    color: var(--text);
    width: 260px;
    outline: none;
    transition: border-color 0.2s;
  }

  .search-box:focus { border-color: var(--gold); }

  .table-controls {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 16px;
    flex-wrap: wrap;
    gap: 12px;
  }

  /* Scrollable table wrapper */
  .table-wrapper { overflow-x: auto; }

  .semester-cols { display: flex; gap: 32px; }

  .sem-col { flex: 1; }

  .sem-title {
    font-size: 13px;
    font-weight: 600;
    color: var(--text-muted);
    text-align: center;
    margin-bottom: 4px;
  }
</style>
</head>
<body>

<!-- ===== LOGIN PAGE ===== -->
<div id="loginPage" class="page">
  <div class="login-card">
    <div class="school-logo">
      <div class="logo-icon">🏫</div>
      <div class="school-name">اعدادية التآخي للبنين</div>
      <div class="school-sub">قسم تربية بيجي — صالح الدين — العراق</div>
    </div>

    <div class="login-title">نتائج الطلاب</div>
    <div class="login-subtitle">للعام الدراسي 2025 – 2026</div>

    <div class="field-group">
      <label>الرقم السري</label>
      <input type="password" id="pinInput" placeholder="أدخل رقمك السري" maxlength="10" autocomplete="off">
    </div>

    <button class="btn-login" onclick="doLogin()">🔐 دخول</button>

    <div class="error-msg" id="errorMsg">❌ الرقم السري غير صحيح، حاول مرة أخرى</div>
  </div>
</div>

<!-- ===== ADMIN PAGE ===== -->
<div id="adminPage" class="page">
  <div class="header">
    <div class="header-brand">
      <div class="header-icon">🏫</div>
      <div class="header-title">لوحة المدير — اعدادية التآخي للبنين</div>
    </div>
    <button class="btn-logout" onclick="logout()">تسجيل خروج</button>
  </div>

  <div class="admin-content">
    <div class="admin-stats">
      <div class="stat-card">
        <div class="stat-num" id="totalStudents">67</div>
        <div class="stat-label">إجمالي الطلاب</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">الرابع</div>
        <div class="stat-label">الصف الدراسي</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">2025–26</div>
        <div class="stat-label">العام الدراسي</div>
      </div>
    </div>

    <div class="table-controls">
      <div class="section-title">📋 قائمة الطلاب وأرقامهم السرية</div>
      <input type="text" class="search-box" placeholder="🔍 ابحث عن طالب..." oninput="filterStudents(this.value)">
    </div>

    <div class="students-table">
      <div class="table-wrapper">
        <table>
          <thead>
            <tr>
              <th>#</th>
              <th>اسم الطالب</th>
              <th>الرقم السري الخاص</th>
              <th>عرض النتيجة</th>
            </tr>
          </thead>
          <tbody id="adminTableBody"></tbody>
        </table>
      </div>
    </div>

    <div style="margin-top:16px; padding:16px; background:rgba(201,168,76,0.08); border:1px solid rgba(201,168,76,0.2); border-radius:12px; font-size:13px; color:#c9a84c;">
      💡 <strong>ملاحظة:</strong> أرسل لكل طالب رقمه السري الخاص ليتمكن من الدخول ومشاهدة نتيجته فقط.
    </div>
  </div>
</div>

<!-- ===== STUDENT RESULT PAGE ===== -->
<div id="studentPage" class="page">
  <div class="header">
    <div class="header-brand">
      <div class="header-icon">📊</div>
      <div class="header-title">كشف النتيجة الدراسية</div>
    </div>
    <button class="btn-logout" onclick="logout()">خروج</button>
  </div>

  <div class="student-content">
    <div class="result-header">
      <div class="academic-year-badge">العام الدراسي 2025 – 2026</div>
      <div class="student-name-display" id="resultName"></div>
      <div class="student-meta">
        <span class="meta-badge">📚 الصف الرابع العلمي</span>
        <span class="meta-badge">🏫 اعدادية التآخي للبنين</span>
        <span class="meta-badge">📍 بيجي — صالح الدين</span>
      </div>
    </div>

    <div class="grades-card">
      <div class="grades-header">📊 درجات الفصل الأول والثاني</div>
      <div class="table-wrapper">
        <table class="grades-table">
          <thead>
            <tr>
              <th>المادة</th>
              <th style="text-align:center">الفصل الأول</th>
              <th style="text-align:center">الفصل الثاني</th>
            </tr>
          </thead>
          <tbody id="gradesBody"></tbody>
        </table>
      </div>
      <div class="footer-note">
        جمهورية العراق — وزارة التربية — المديرية العامة لتربية صالح الدين<br>
        المدير: خالد رسول فهد
      </div>
    </div>
  </div>
</div>

<script>
// ==================== DATA ====================
const ADMIN_PIN = "ali2027";

const students = [
  { id:1,  name:"ابراهيم شهاب احمد عبدالله",     pin:"ST2601", sem1:{اسلامية:80,عربية:40,انجليزية:50,رياضيات:40,كيمياء:65,فيزياء:37,احياء:71,بعث:72,رياضة:70,فنية:70}, sem2:{اسلامية:68,عربية:66,انجليزية:66,رياضيات:41,كيمياء:42,فيزياء:61,احياء:42,بعث:95,رياضة:70,فنية:70} },
  { id:2,  name:"احمد جمال ناصر",                  pin:"ST2602", sem1:{اسلامية:25,عربية:27,انجليزية:30,رياضيات:25,كيمياء:33,فيزياء:32,احياء:25,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:33,عربية:24,انجليزية:39,رياضيات:11,كيمياء:8,فيزياء:19,احياء:26,بعث:20,رياضة:60,فنية:60} },
  { id:3,  name:"احمد خلف محمد ابراهيم",           pin:"ST2603", sem1:{اسلامية:56,عربية:27,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:33,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:66,عربية:null,انجليزية:58,رياضيات:10,كيمياء:12,فيزياء:19,احياء:25,بعث:65,رياضة:60,فنية:60} },
  { id:4,  name:"اسامة سعيد عايد",                 pin:"ST2604", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:37,عربية:null,انجليزية:null,رياضيات:null,كيمياء:null,فيزياء:null,احياء:null,بعث:null,رياضة:60,فنية:60} },
  { id:5,  name:"اسحاق عبدالله نجم عبدالله",       pin:"ST2605", sem1:{اسلامية:100,عربية:60,انجليزية:60,رياضيات:42,كيمياء:40,فيزياء:75,احياء:59,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:76,عربية:50,انجليزية:57,رياضيات:33,كيمياء:30,فيزياء:61,احياء:39,بعث:70,رياضة:70,فنية:70} },
  { id:6,  name:"امير مزاحم احمد حمود",             pin:"ST2606", sem1:{اسلامية:92,عربية:65,انجليزية:97,رياضيات:43,كيمياء:38,فيزياء:75,احياء:68,بعث:85,رياضة:70,فنية:70}, sem2:{اسلامية:80,عربية:67,انجليزية:85,رياضيات:51,كيمياء:35,فيزياء:68,احياء:57,بعث:55,رياضة:70,فنية:70} },
  { id:7,  name:"انس سعيد عايد جاسم",              pin:"ST2607", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:29,احياء:25,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:40,عربية:39,انجليزية:50,رياضيات:7,كيمياء:11,فيزياء:null,احياء:12,بعث:21,رياضة:60,فنية:60} },
  { id:8,  name:"انس ماجد صايل شلال",              pin:"ST2608", sem1:{اسلامية:93,عربية:80,انجليزية:97,رياضيات:25,كيمياء:42,فيزياء:85,احياء:62,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:95,عربية:60,انجليزية:95,رياضيات:23,كيمياء:22,فيزياء:69,احياء:54,بعث:75,رياضة:70,فنية:70} },
  { id:9,  name:"ثامر ياسين سالم",                 pin:"ST2609", sem1:{اسلامية:23,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:null,عربية:null,انجليزية:null,رياضيات:null,كيمياء:null,فيزياء:null,احياء:null,بعث:null,رياضة:null,فنية:null} },
  { id:10, name:"جبار علي جبار بكر",               pin:"ST2610", sem1:{اسلامية:95,عربية:68,انجليزية:75,رياضيات:42,كيمياء:67,فيزياء:70,احياء:89,بعث:70,رياضة:70,فنية:70}, sem2:{اسلامية:71,عربية:65,انجليزية:81,رياضيات:37,كيمياء:27,فيزياء:71,احياء:32,بعث:90,رياضة:70,فنية:70} },
  { id:11, name:"حسام باسل جاسم ابراهيم",          pin:"ST2611", sem1:{اسلامية:70,عربية:50,انجليزية:55,رياضيات:30,كيمياء:31,فيزياء:50,احياء:57,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:77,عربية:66,انجليزية:51,رياضيات:24,كيمياء:42,فيزياء:50,احياء:59,بعث:80,رياضة:60,فنية:60} },
  { id:12, name:"حسن جاسم حسن محمد",               pin:"ST2612", sem1:{اسلامية:75,عربية:25,انجليزية:30,رياضيات:27,كيمياء:34,فيزياء:26,احياء:35,بعث:70,رياضة:60,فنية:60}, sem2:{اسلامية:59,عربية:29,انجليزية:59,رياضيات:16,كيمياء:14,فيزياء:28,احياء:32,بعث:60,رياضة:60,فنية:60} },
  { id:13, name:"حسين محمد فرحان",                 pin:"ST2613", sem1:{اسلامية:55,عربية:29,انجليزية:30,رياضيات:25,كيمياء:37,فيزياء:25,احياء:50,بعث:75,رياضة:60,فنية:60}, sem2:{اسلامية:57,عربية:20,انجليزية:51,رياضيات:12,كيمياء:10,فيزياء:25,احياء:20,بعث:18,رياضة:60,فنية:60} },
  { id:14, name:"ذاكر مقداد عبدالله شجاع",         pin:"ST2614", sem1:{اسلامية:80,عربية:75,انجليزية:50,رياضيات:34,كيمياء:60,فيزياء:35,احياء:60,بعث:80,رياضة:70,فنية:70}, sem2:{اسلامية:71,عربية:41,انجليزية:52,رياضيات:13,كيمياء:24,فيزياء:34,احياء:31,بعث:50,رياضة:70,فنية:70} },
  { id:15, name:"ذو الفقار سعدون حمادي صالح",      pin:"ST2615", sem1:{اسلامية:90,عربية:63,انجليزية:80,رياضيات:54,كيمياء:75,فيزياء:100,احياء:94,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:100,عربية:72,انجليزية:78,رياضيات:51,كيمياء:37,فيزياء:75,احياء:57,بعث:95,رياضة:100,فنية:100} },
  { id:16, name:"رأفت حمادي سليم محمود",           pin:"ST2616", sem1:{اسلامية:100,عربية:78,انجليزية:95,رياضيات:59,كيمياء:63,فيزياء:55,احياء:79,بعث:95,رياضة:100,فنية:100}, sem2:{اسلامية:80,عربية:73,انجليزية:83,رياضيات:55,كيمياء:65,فيزياء:86,احياء:68,بعث:90,رياضة:100,فنية:100} },
  { id:17, name:"رافع حمادي سليم محمود",           pin:"ST2617", sem1:{اسلامية:93,عربية:83,انجليزية:75,رياضيات:50,كيمياء:51,فيزياء:55,احياء:79,بعث:80,رياضة:70,فنية:70}, sem2:{اسلامية:90,عربية:66,انجليزية:82,رياضيات:60,كيمياء:41,فيزياء:59,احياء:50,بعث:90,رياضة:70,فنية:70} },
  { id:18, name:"رمضان غانم عارف",                 pin:"ST2618", sem1:{اسلامية:100,عربية:71,انجليزية:65,رياضيات:51,كيمياء:57,فيزياء:100,احياء:84,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:85,عربية:76,انجليزية:73,رياضيات:35,كيمياء:56,فيزياء:67,احياء:60,بعث:70,رياضة:100,فنية:100} },
  { id:19, name:"زياد غايب عايد جاسم",             pin:"ST2619", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:80,رياضة:60,فنية:60}, sem2:{اسلامية:39,عربية:19,انجليزية:29,رياضيات:10,كيمياء:14,فيزياء:9,احياء:19,بعث:15,رياضة:60,فنية:60} },
  { id:20, name:"سراقة فائق ياسين بكر",            pin:"ST2620", sem1:{اسلامية:98,عربية:65,انجليزية:75,رياضيات:87,كيمياء:75,فيزياء:100,احياء:95,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:98,عربية:82,انجليزية:78,رياضيات:84,كيمياء:61,فيزياء:87,احياء:76,بعث:98,رياضة:100,فنية:100} },
  { id:21, name:"سعد فؤاد عطية عبدالله",           pin:"ST2621", sem1:{اسلامية:100,عربية:65,انجليزية:50,رياضيات:68,كيمياء:63,فيزياء:50,احياء:78,بعث:85,رياضة:80,فنية:80}, sem2:{اسلامية:80,عربية:74,انجليزية:61,رياضيات:69,كيمياء:null,فيزياء:23,احياء:60,بعث:50,رياضة:80,فنية:80} },
  { id:22, name:"سيف عماد خلف طعمة",               pin:"ST2622", sem1:{اسلامية:68,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:76,عربية:50,انجليزية:60,رياضيات:23,كيمياء:12,فيزياء:30,احياء:18,بعث:50,رياضة:60,فنية:60} },
  { id:23, name:"سيف مزاحم احمد حمود",             pin:"ST2623", sem1:{اسلامية:98,عربية:59,انجليزية:95,رياضيات:41,كيمياء:58,فيزياء:72,احياء:78,بعث:85,رياضة:80,فنية:80}, sem2:{اسلامية:85,عربية:84,انجليزية:84,رياضيات:61,كيمياء:31,فيزياء:75,احياء:57,بعث:65,رياضة:80,فنية:80} },
  { id:24, name:"صالح مهدي حميد انصيف",            pin:"ST2624", sem1:{اسلامية:100,عربية:78,انجليزية:98,رياضيات:93,كيمياء:96,فيزياء:100,احياء:95,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:95,عربية:84,انجليزية:96,رياضيات:91,كيمياء:78,فيزياء:79,احياء:77,بعث:95,رياضة:100,فنية:100} },
  { id:25, name:"صهيب جاسم احمد عبدالله",          pin:"ST2625", sem1:{اسلامية:75,عربية:50,انجليزية:40,رياضيات:31,كيمياء:42,فيزياء:50,احياء:79,بعث:100,رياضة:70,فنية:70}, sem2:{اسلامية:75,عربية:64,انجليزية:50,رياضيات:32,كيمياء:20,فيزياء:52,احياء:39,بعث:60,رياضة:70,فنية:70} },
  { id:26, name:"صهيب عدنان دخيل ضاحي",            pin:"ST2626", sem1:{اسلامية:100,عربية:75,انجليزية:80,رياضيات:75,كيمياء:65,فيزياء:70,احياء:87,بعث:100,رياضة:80,فنية:80}, sem2:{اسلامية:98,عربية:88,انجليزية:75,رياضيات:69,كيمياء:68,فيزياء:84,احياء:66,بعث:85,رياضة:80,فنية:80} },
  { id:27, name:"ضرغام علي احمد حمود",             pin:"ST2627", sem1:{اسلامية:78,عربية:40,انجليزية:50,رياضيات:25,كيمياء:36,فيزياء:26,احياء:36,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:71,عربية:50,انجليزية:60,رياضيات:19,كيمياء:19,فيزياء:25,احياء:22,بعث:55,رياضة:60,فنية:60} },
  { id:28, name:"عارف ضياء حسين مطلق",             pin:"ST2628", sem1:{اسلامية:100,عربية:62,انجليزية:75,رياضيات:34,كيمياء:42,فيزياء:75,احياء:58,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:88,عربية:76,انجليزية:70,رياضيات:36,كيمياء:40,فيزياء:76,احياء:78,بعث:60,رياضة:70,فنية:70} },
  { id:29, name:"عباس حمود جدوع خلف",              pin:"ST2629", sem1:{اسلامية:98,عربية:74,انجليزية:60,رياضيات:54,كيمياء:52,فيزياء:52,احياء:67,بعث:100,رياضة:90,فنية:90}, sem2:{اسلامية:76,عربية:82,انجليزية:62,رياضيات:56,كيمياء:38,فيزياء:93,احياء:71,بعث:60,رياضة:90,فنية:90} },
  { id:30, name:"عبدالرحمن ضياء خلف",              pin:"ST2630", sem1:{اسلامية:25,عربية:33,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:32,احياء:25,بعث:85,رياضة:60,فنية:60}, sem2:{اسلامية:59,عربية:55,انجليزية:40,رياضيات:17,كيمياء:17,فيزياء:36,احياء:18,بعث:54,رياضة:60,فنية:60} },
  { id:31, name:"عبدالقادر مثنى هاشم حسين",        pin:"ST2631", sem1:{اسلامية:100,عربية:55,انجليزية:80,رياضيات:56,كيمياء:61,فيزياء:100,احياء:86,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:95,عربية:75,انجليزية:72,رياضيات:50,كيمياء:59,فيزياء:50,احياء:71,بعث:85,رياضة:100,فنية:100} },
  { id:32, name:"عبدالرحمن نمير محمد",              pin:"ST2632", sem1:{اسلامية:75,عربية:25,انجليزية:40,رياضيات:25,كيمياء:40,فيزياء:50,احياء:50,بعث:85,رياضة:70,فنية:70}, sem2:{اسلامية:57,عربية:34,انجليزية:52,رياضيات:16,كيمياء:15,فيزياء:25,احياء:12,بعث:21,رياضة:70,فنية:70} },
  { id:33, name:"عبدالكريم فارس ابراهيم",          pin:"ST2633", sem1:{اسلامية:68,عربية:40,انجليزية:25,رياضيات:25,كيمياء:35,فيزياء:32,احياء:34,بعث:75,رياضة:60,فنية:60}, sem2:{اسلامية:58,عربية:58,انجليزية:27,رياضيات:15,كيمياء:15,فيزياء:21,احياء:25,بعث:68,رياضة:60,فنية:60} },
  { id:34, name:"عبدالله ادهام ابراهيم",           pin:"ST2634", sem1:{اسلامية:25,عربية:25,انجليزية:30,رياضيات:25,كيمياء:25,فيزياء:25,احياء:35,بعث:85,رياضة:60,فنية:60}, sem2:{اسلامية:84,عربية:44,انجليزية:55,رياضيات:19,كيمياء:14,فيزياء:17,احياء:13,بعث:60,رياضة:60,فنية:60} },
  { id:35, name:"عبدالملك جاسم سبتي",              pin:"ST2635", sem1:{اسلامية:90,عربية:50,انجليزية:60,رياضيات:53,كيمياء:53,فيزياء:67,احياء:70,بعث:95,رياضة:70,فنية:70}, sem2:{اسلامية:88,عربية:52,انجليزية:41,رياضيات:27,كيمياء:21,فيزياء:38,احياء:22,بعث:80,رياضة:70,فنية:70} },
  { id:36, name:"عساف عماد عطية عبدالله",          pin:"ST2636", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:38,فيزياء:30,احياء:25,بعث:70,رياضة:60,فنية:60}, sem2:{اسلامية:13,عربية:21,انجليزية:50,رياضيات:10,كيمياء:8,فيزياء:19,احياء:17,بعث:25,رياضة:60,فنية:60} },
  { id:37, name:"علي سعدون حمادي صالح",            pin:"ST2637", sem1:{اسلامية:82,عربية:65,انجليزية:55,رياضيات:41,كيمياء:50,فيزياء:55,احياء:66,بعث:80,رياضة:60,فنية:60}, sem2:{اسلامية:79,عربية:68,انجليزية:53,رياضيات:33,كيمياء:32,فيزياء:30,احياء:29,بعث:70,رياضة:60,فنية:60} },
  { id:38, name:"علي محمود حسين محمود",            pin:"ST2638", sem1:{اسلامية:78,عربية:73,انجليزية:70,رياضيات:35,كيمياء:40,فيزياء:100,احياء:67,بعث:95,رياضة:70,فنية:70}, sem2:{اسلامية:88,عربية:68,انجليزية:63,رياضيات:20,كيمياء:29,فيزياء:60,احياء:52,بعث:75,رياضة:70,فنية:70} },
  { id:39, name:"علي مزاحم احمد حمود",             pin:"ST2639", sem1:{اسلامية:100,عربية:67,انجليزية:85,رياضيات:25,كيمياء:50,فيزياء:79,احياء:63,بعث:97,رياضة:90,فنية:90}, sem2:{اسلامية:61,عربية:55,انجليزية:57,رياضيات:15,كيمياء:23,فيزياء:16,احياء:25,بعث:65,رياضة:90,فنية:90} },
  { id:40, name:"عمر خالد حمود احمد",              pin:"ST2640", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:15,عربية:21,انجليزية:9,رياضيات:10,كيمياء:12,فيزياء:11,احياء:15,بعث:17,رياضة:60,فنية:60} },
  { id:41, name:"عمر نجم جاسم محمد",               pin:"ST2641", sem1:{اسلامية:80,عربية:29,انجليزية:40,رياضيات:25,كيمياء:36,فيزياء:50,احياء:34,بعث:85,رياضة:60,فنية:60}, sem2:{اسلامية:42,عربية:46,انجليزية:20,رياضيات:36,كيمياء:19,فيزياء:51,احياء:19,بعث:80,رياضة:60,فنية:60} },
  { id:42, name:"عمران يونس احمد عبدالله",         pin:"ST2642", sem1:{اسلامية:100,عربية:60,انجليزية:55,رياضيات:25,كيمياء:39,فيزياء:37,احياء:64,بعث:95,رياضة:70,فنية:70}, sem2:{اسلامية:70,عربية:61,انجليزية:55,رياضيات:26,كيمياء:27,فيزياء:53,احياء:40,بعث:55,رياضة:70,فنية:70} },
  { id:43, name:"غزوان عنتر حمد خلف",              pin:"ST2643", sem1:{اسلامية:90,عربية:67,انجليزية:70,رياضيات:50,كيمياء:55,فيزياء:90,احياء:90,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:69,عربية:70,انجليزية:57,رياضيات:20,كيمياء:38,فيزياء:50,احياء:57,بعث:90,رياضة:100,فنية:100} },
  { id:44, name:"فرحان صالح ابراهيم",              pin:"ST2644", sem1:{اسلامية:25,عربية:25,انجليزية:null,رياضيات:null,كيمياء:null,فيزياء:null,احياء:null,بعث:null,رياضة:null,فنية:null}, sem2:{اسلامية:null,عربية:null,انجليزية:null,رياضيات:null,كيمياء:null,فيزياء:null,احياء:null,بعث:null,رياضة:null,فنية:null} },
  { id:45, name:"فهد زياد خلف عبدالله",            pin:"ST2645", sem1:{اسلامية:70,عربية:50,انجليزية:30,رياضيات:25,كيمياء:35,فيزياء:25,احياء:33,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:61,عربية:45,انجليزية:52,رياضيات:12,كيمياء:11,فيزياء:33,احياء:19,بعث:20,رياضة:60,فنية:60} },
  { id:46, name:"فواز جاسم عتيج جاسم",             pin:"ST2646", sem1:{اسلامية:85,عربية:50,انجليزية:50,رياضيات:30,كيمياء:44,فيزياء:80,احياء:60,بعث:85,رياضة:70,فنية:70}, sem2:{اسلامية:69,عربية:59,انجليزية:53,رياضيات:17,كيمياء:31,فيزياء:46,احياء:36,بعث:80,رياضة:70,فنية:70} },
  { id:47, name:"محمد انور ابراهيم سعدون",         pin:"ST2647", sem1:{اسلامية:100,عربية:69,انجليزية:40,رياضيات:44,كيمياء:56,فيزياء:82,احياء:51,بعث:85,رياضة:70,فنية:70}, sem2:{اسلامية:63,عربية:55,انجليزية:42,رياضيات:11,كيمياء:12,فيزياء:38,احياء:24,بعث:80,رياضة:70,فنية:70} },
  { id:48, name:"محمد ضياء حسين",                  pin:"ST2648", sem1:{اسلامية:100,عربية:68,انجليزية:55,رياضيات:33,كيمياء:43,فيزياء:54,احياء:52,بعث:75,رياضة:60,فنية:60}, sem2:{اسلامية:67,عربية:52,انجليزية:56,رياضيات:45,كيمياء:14,فيزياء:36,احياء:23,بعث:45,رياضة:60,فنية:60} },
  { id:49, name:"محمد فواز شهاب احمد",             pin:"ST2649", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:33,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:18,عربية:24,انجليزية:28,رياضيات:10,كيمياء:14,فيزياء:16,احياء:13,بعث:50,رياضة:60,فنية:60} },
  { id:50, name:"محمد ناجي هبود طعمة",             pin:"ST2650", sem1:{اسلامية:100,عربية:25,انجليزية:30,رياضيات:25,كيمياء:36,فيزياء:26,احياء:33,بعث:76,رياضة:60,فنية:60}, sem2:{اسلامية:71,عربية:38,انجليزية:45,رياضيات:13,كيمياء:40,فيزياء:30,احياء:26,بعث:65,رياضة:60,فنية:60} },
  { id:51, name:"محمود رائد حسن محمد",             pin:"ST2651", sem1:{اسلامية:95,عربية:85,انجليزية:50,رياضيات:60,كيمياء:67,فيزياء:100,احياء:94,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:85,عربية:68,انجليزية:98,رياضيات:64,كيمياء:83,فيزياء:80,احياء:67,بعث:80,رياضة:100,فنية:100} },
  { id:52, name:"محمود علي احمد حسين",             pin:"ST2652", sem1:{اسلامية:100,عربية:87,انجليزية:98,رياضيات:76,كيمياء:78,فيزياء:95,احياء:99,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:85,عربية:81,انجليزية:89,رياضيات:54,كيمياء:58,فيزياء:68,احياء:78,بعث:80,رياضة:100,فنية:100} },
  { id:53, name:"محمود فواز شهاب احمد",            pin:"ST2653", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:13,عربية:17,انجليزية:25,رياضيات:10,كيمياء:14,فيزياء:7,احياء:12,بعث:25,رياضة:60,فنية:60} },
  { id:54, name:"مشتاق طالب منهي شيحان",           pin:"ST2654", sem1:{اسلامية:100,عربية:83,انجليزية:98,رياضيات:78,كيمياء:91,فيزياء:100,احياء:98,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:79,عربية:92,انجليزية:84,رياضيات:61,كيمياء:51,فيزياء:98,احياء:84,بعث:90,رياضة:100,فنية:100} },
  { id:55, name:"مصطفى حسين طلال عباس",            pin:"ST2655", sem1:{اسلامية:60,عربية:50,انجليزية:25,رياضيات:28,كيمياء:42,فيزياء:29,احياء:39,بعث:75,رياضة:60,فنية:60}, sem2:{اسلامية:66,عربية:45,انجليزية:33,رياضيات:12,كيمياء:14,فيزياء:38,احياء:16,بعث:15,رياضة:60,فنية:60} },
  { id:56, name:"مظفر طارق مطر عطية",              pin:"ST2656", sem1:{اسلامية:100,عربية:73,انجليزية:98,رياضيات:39,كيمياء:95,فيزياء:100,احياء:79,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:81,عربية:81,انجليزية:77,رياضيات:50,كيمياء:59,فيزياء:100,احياء:73,بعث:80,رياضة:100,فنية:100} },
  { id:57, name:"هارون ذياب احمد عبدالله",         pin:"ST2657", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:42,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:30,عربية:20,انجليزية:25,رياضيات:18,كيمياء:21,فيزياء:16,احياء:21,بعث:55,رياضة:60,فنية:60} },
  { id:58, name:"هاشم عماد علي",                   pin:"ST2658", sem1:{اسلامية:90,عربية:37,انجليزية:55,رياضيات:26,كيمياء:25,فيزياء:26,احياء:54,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:77,عربية:43,انجليزية:54,رياضيات:15,كيمياء:25,فيزياء:28,احياء:36,بعث:85,رياضة:60,فنية:60} },
  { id:59, name:"هذال عباس شرقي ضاحي",             pin:"ST2659", sem1:{اسلامية:85,عربية:60,انجليزية:50,رياضيات:32,كيمياء:57,فيزياء:75,احياء:69,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:80,عربية:77,انجليزية:56,رياضيات:22,كيمياء:37,فيزياء:52,احياء:39,بعث:65,رياضة:70,فنية:70} },
  { id:60, name:"هيلان دحام حسين موسى",            pin:"ST2660", sem1:{اسلامية:25,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:25,احياء:25,بعث:50,رياضة:60,فنية:60}, sem2:{اسلامية:53,عربية:26,انجليزية:26,رياضيات:12,كيمياء:7,فيزياء:22,احياء:23,بعث:45,رياضة:60,فنية:60} },
  { id:61, name:"وسام نصرالله دخيل ضاحي",          pin:"ST2661", sem1:{اسلامية:90,عربية:70,انجليزية:90,رياضيات:50,كيمياء:56,فيزياء:75,احياء:89,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:98,عربية:78,انجليزية:96,رياضيات:50,كيمياء:38,فيزياء:55,احياء:40,بعث:85,رياضة:70,فنية:70} },
  { id:62, name:"ياسر عامر حمد خلف",               pin:"ST2662", sem1:{اسلامية:100,عربية:65,انجليزية:40,رياضيات:36,كيمياء:37,فيزياء:27,احياء:70,بعث:80,رياضة:60,فنية:60}, sem2:{اسلامية:69,عربية:79,انجليزية:50,رياضيات:8,كيمياء:36,فيزياء:44,احياء:52,بعث:80,رياضة:60,فنية:60} },
  { id:63, name:"يحيى عدنان حميد",                 pin:"ST2663", sem1:{اسلامية:58,عربية:40,انجليزية:40,رياضيات:25,كيمياء:40,فيزياء:40,احياء:38,بعث:95,رياضة:60,فنية:60}, sem2:{اسلامية:68,عربية:58,انجليزية:50,رياضيات:41,كيمياء:18,فيزياء:39,احياء:39,بعث:60,رياضة:60,فنية:60} },
  { id:64, name:"يعقوب سمير محمد مطلق",            pin:"ST2664", sem1:{اسلامية:90,عربية:27,انجليزية:25,رياضيات:25,كيمياء:40,فيزياء:30,احياء:40,بعث:75,رياضة:60,فنية:60}, sem2:{اسلامية:28,عربية:33,انجليزية:46,رياضيات:2,كيمياء:12,فيزياء:22,احياء:19,بعث:55,رياضة:60,فنية:60} },
  { id:65, name:"يوسف رائد خضير جاسم",             pin:"ST2665", sem1:{اسلامية:100,عربية:82,انجليزية:60,رياضيات:43,كيمياء:65,فيزياء:100,احياء:85,بعث:100,رياضة:100,فنية:100}, sem2:{اسلامية:89,عربية:86,انجليزية:70,رياضيات:60,كيمياء:75,فيزياء:97,احياء:54,بعث:90,رياضة:100,فنية:100} },
  { id:66, name:"يوسف علي عيد علي",                pin:"ST2666", sem1:{اسلامية:75,عربية:42,انجليزية:25,رياضيات:40,كيمياء:25,فيزياء:35,احياء:42,بعث:75,رياضة:70,فنية:70}, sem2:{اسلامية:51,عربية:27,انجليزية:50,رياضيات:18,كيمياء:12,فيزياء:17,احياء:23,بعث:55,رياضة:70,فنية:70} },
  { id:67, name:"يوسف نزهان مزبان طالب",           pin:"ST2667", sem1:{اسلامية:55,عربية:50,انجليزية:40,رياضيات:25,كيمياء:32,فيزياء:29,احياء:25,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:64,عربية:44,انجليزية:53,رياضيات:14,كيمياء:13,فيزياء:22,احياء:28,بعث:70,رياضة:60,فنية:60} },
  { id:68, name:"يوسف قيس احمد محمد",              pin:"ST2668", sem1:{اسلامية:75,عربية:25,انجليزية:25,رياضيات:25,كيمياء:25,فيزياء:26,احياء:25,بعث:65,رياضة:60,فنية:60}, sem2:{اسلامية:61,عربية:28,انجليزية:58,رياضيات:8,كيمياء:14,فيزياء:37,احياء:32,بعث:65,رياضة:60,فنية:60} },
];

const subjectLabels = {
  اسلامية:"التربية الإسلامية",
  عربية:"اللغة العربية",
  انجليزية:"اللغة الإنكليزية",
  رياضيات:"الرياضيات",
  كيمياء:"الكيمياء",
  فيزياء:"الفيزياء",
  احياء:"علم الأحياء",
  بعث:"جرائم حزب البعث",
  رياضة:"التربية الرياضية",
  فنية:"التربية الفنية"
};

// Build PIN lookup
const pinMap = {};
pinMap[ADMIN_PIN] = "admin";
students.forEach(s => { pinMap[s.pin] = s.id; });

let currentUser = null;

// ===== LOGIN =====
function doLogin() {
  const pin = document.getElementById('pinInput').value.trim();
  const errEl = document.getElementById('errorMsg');

  if (!pin) { showError("الرجاء إدخال الرقم السري"); return; }

  if (pinMap[pin] !== undefined) {
    errEl.classList.remove('show');
    currentUser = pinMap[pin];
    if (currentUser === "admin") {
      showAdminPage();
    } else {
      showStudentPage(currentUser);
    }
  } else {
    showError("الرقم السري غير صحيح، حاول مرة أخرى");
    document.getElementById('pinInput').value = '';
  }
}

document.getElementById('pinInput').addEventListener('keydown', e => {
  if (e.key === 'Enter') doLogin();
});

function showError(msg) {
  const el = document.getElementById('errorMsg');
  el.textContent = "❌ " + msg;
  el.classList.remove('show');
  void el.offsetWidth;
  el.classList.add('show');
}

// ===== ADMIN PAGE =====
function showAdminPage() {
  document.getElementById('loginPage').style.display = 'none';
  document.getElementById('adminPage').style.display = 'block';
  document.getElementById('totalStudents').textContent = students.length;
  renderAdminTable(students);
}

function renderAdminTable(list) {
  const tbody = document.getElementById('adminTableBody');
  tbody.innerHTML = list.map(s => `
    <tr>
      <td style="color:var(--text-muted);font-size:13px">${s.id}</td>
      <td style="font-weight:600">${s.name}</td>
      <td><span class="pin-badge">${s.pin}</span></td>
      <td><button class="view-btn" onclick="viewStudentAsAdmin(${s.id})">عرض النتيجة 👁</button></td>
    </tr>
  `).join('');
}

function filterStudents(q) {
  const filtered = students.filter(s => s.name.includes(q) || s.pin.includes(q));
  renderAdminTable(filtered);
}

function viewStudentAsAdmin(id) {
  showStudentPage(id, true);
}

// ===== STUDENT PAGE =====
function showStudentPage(id, fromAdmin) {
  const student = students.find(s => s.id === id);
  if (!student) return;

  document.getElementById('loginPage').style.display = 'none';
  document.getElementById('adminPage').style.display = 'none';
  document.getElementById('studentPage').style.display = 'block';

  document.getElementById('resultName').textContent = student.name;

  const subjects = Object.keys(subjectLabels);
  const tbody = document.getElementById('gradesBody');

  tbody.innerHTML = subjects.map(key => {
    const g1 = student.sem1[key];
    const g2 = student.sem2[key];

    return `
      <tr>
        <td class="subject-name">${subjectLabels[key]}</td>
        <td>${renderGrade(g1)}</td>
        <td>${renderGrade(g2)}</td>
      </tr>
    `;
  }).join('');

  // Add back button if admin viewing
  const backBtn = document.getElementById('backBtn');
  if (fromAdmin) {
    if (!backBtn) {
      const btn = document.createElement('button');
      btn.id = 'backBtn';
      btn.className = 'btn-logout';
      btn.textContent = '← العودة للقائمة';
      btn.onclick = () => {
        document.getElementById('studentPage').style.display = 'none';
        document.getElementById('adminPage').style.display = 'block';
      };
      document.querySelector('#studentPage .header').appendChild(btn);
    }
  } else {
    if (backBtn) backBtn.remove();
  }
}

function renderGrade(g) {
  if (g === null || g === undefined) return `<span style="color:var(--text-muted);font-size:13px">—</span>`;
  const pct = g;
  let cls = 'grade-high';
  let barColor = '#3fb950';
  if (pct < 50) { cls = 'grade-low'; barColor = '#f85149'; }
  else if (pct < 70) { cls = 'grade-mid'; barColor = '#d29922'; }

  return `
    <div style="display:flex;align-items:center;gap:8px;justify-content:center">
      <span class="grade-bar-wrap">
        <span class="grade-bar" style="width:${pct}%;background:${barColor}"></span>
      </span>
      <span class="grade-num ${cls}">${g}</span>
    </div>`;
}

function logout() {
  currentUser = null;
  document.getElementById('loginPage').style.display = 'flex';
  document.getElementById('adminPage').style.display = 'none';
  document.getElementById('studentPage').style.display = 'none';
  document.getElementById('pinInput').value = '';
  document.getElementById('errorMsg').classList.remove('show');
}
</script>
</body>
</html>
