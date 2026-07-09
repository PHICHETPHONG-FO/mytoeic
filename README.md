# mytoeic
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TOEIC 2 เดือน พิชิตเป้า | 60-Day TOEIC Quest</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Kanit:wght@400;500;600;700;800&family=Sarabun:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0f1729; --bg2:#141d33; --card:#1b2942; --card2:#22314f;
    --ink:#eaf0ff; --muted:#93a4c8; --line:#2b3c5e;
    --brand:#6c5ce7; --brand2:#a55eea; --accent:#00d2a8; --gold:#ffd23f;
    --hot:#ff6b6b; --blue:#4da3ff; --purple:#a55eea; --orange:#ff9f43;
    --green:#26de81; --pink:#fd79a8; --indigo:#5f6bff; --teal:#00d2a8;
    --radius:18px; --shadow:0 10px 30px rgba(0,0,0,.35);
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    margin:0; font-family:'Sarabun',system-ui,sans-serif; color:var(--ink);
    background:
      radial-gradient(1100px 500px at 85% -10%, rgba(108,92,231,.28), transparent 60%),
      radial-gradient(900px 500px at -10% 10%, rgba(0,210,168,.18), transparent 55%),
      var(--bg);
    line-height:1.6;
  }
  h1,h2,h3,h4,.font-head{font-family:'Kanit',sans-serif;font-weight:700;letter-spacing:.2px}
  .wrap{max-width:1080px;margin:0 auto;padding:22px 18px 80px}
  a{color:var(--accent)}

  /* ---------- HERO ---------- */
  .hero{
    background:linear-gradient(135deg,#6c5ce7 0%,#a55eea 45%,#00b894 130%);
    border-radius:26px;padding:30px 28px;position:relative;overflow:hidden;
    box-shadow:var(--shadow);
  }
  .hero:after{content:"";position:absolute;inset:0;background:
    radial-gradient(400px 200px at 90% 10%, rgba(255,255,255,.18), transparent 60%);pointer-events:none}
  .hero .badge-teacher{display:inline-flex;align-items:center;gap:8px;background:rgba(0,0,0,.22);
    padding:6px 14px;border-radius:999px;font-size:13px;font-weight:600;margin-bottom:12px}
  .hero h1{font-size:34px;margin:.1em 0 .15em;font-weight:800;line-height:1.15}
  .hero p{margin:.2em 0;max-width:720px;color:#f3f0ff}
  .hero .sub{font-size:14px;color:#e7e0ff;opacity:.95}
  .quote{margin-top:16px;background:rgba(0,0,0,.20);border-left:4px solid var(--gold);
    padding:12px 16px;border-radius:12px;font-style:italic;font-size:14.5px}

  /* ---------- DASHBOARD ---------- */
  .dash{display:grid;grid-template-columns:1.4fr 1fr;gap:16px;margin-top:18px}
  @media(max-width:820px){.dash{grid-template-columns:1fr}}
  .card{background:var(--card);border:1px solid var(--line);border-radius:var(--radius);
    padding:20px;box-shadow:var(--shadow)}
  .lvl-top{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
  .rank{display:flex;align-items:center;gap:14px}
  .rank .ring{width:66px;height:66px;border-radius:50%;display:grid;place-items:center;
    font-size:30px;background:conic-gradient(var(--gold) var(--deg,0deg), #2c3c5e 0deg);
    position:relative;flex:0 0 auto}
  .rank .ring:after{content:"";position:absolute;inset:6px;border-radius:50%;background:var(--card)}
  .rank .ring span{position:relative;z-index:1}
  .rank .name{font-family:'Kanit';font-weight:700;font-size:19px}
  .rank .name small{display:block;font-family:'Sarabun';font-weight:500;color:var(--muted);font-size:12.5px}
  .xp-num{text-align:right}
  .xp-num b{font-family:'Kanit';font-size:26px;color:var(--gold)}
  .xp-num small{display:block;color:var(--muted);font-size:12px}
  .bar{height:14px;background:#0e1626;border-radius:999px;overflow:hidden;margin-top:16px;border:1px solid var(--line)}
  .bar > i{display:block;height:100%;width:0;border-radius:999px;
    background:linear-gradient(90deg,var(--accent),var(--gold));transition:width .6s cubic-bezier(.2,.8,.2,1)}
  .bar-label{display:flex;justify-content:space-between;font-size:12px;color:var(--muted);margin-top:6px}

  .stats{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
  .stat{background:var(--card2);border:1px solid var(--line);border-radius:14px;padding:14px;text-align:center}
  .stat b{font-family:'Kanit';font-size:24px;display:block}
  .stat small{color:var(--muted);font-size:12px}
  .stat.streak b{color:var(--hot)} .stat.days b{color:var(--accent)}
  .stat.pct b{color:var(--gold)} .stat.tasks b{color:var(--blue)}

  /* ---------- ACHIEVEMENTS ---------- */
  .ach-wrap{margin-top:16px}
  .section-title{display:flex;align-items:center;gap:10px;margin:26px 0 12px}
  .section-title h2{font-size:22px;margin:0}
  .section-title .line{flex:1;height:1px;background:var(--line)}
  .badges{display:flex;flex-wrap:wrap;gap:10px}
  .bdg{display:flex;align-items:center;gap:9px;background:var(--card);border:1px solid var(--line);
    border-radius:14px;padding:10px 14px;opacity:.4;filter:grayscale(.8);transition:.3s;min-width:0}
  .bdg.on{opacity:1;filter:none;border-color:var(--gold);box-shadow:0 0 0 1px var(--gold) inset,0 6px 16px rgba(255,210,63,.15)}
  .bdg .em{font-size:22px}
  .bdg .t{font-size:12.5px;font-weight:600;line-height:1.25}
  .bdg .t small{display:block;color:var(--muted);font-weight:400;font-size:11px}

  /* ---------- INFO CARDS ---------- */
  .info-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
  @media(max-width:820px){.info-grid{grid-template-columns:1fr}}
  .info h3{margin:0 0 8px;font-size:17px;display:flex;align-items:center;gap:8px}
  .info ul{margin:8px 0 0;padding-left:20px}
  .info li{margin:5px 0;font-size:14px}
  .pill-row{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
  .pill{font-size:12px;background:var(--card2);border:1px solid var(--line);padding:5px 11px;border-radius:999px}

  /* ---------- WEEK ACCORDION ---------- */
  .week{border-radius:var(--radius);margin-bottom:14px;overflow:hidden;border:1px solid var(--line);
    background:var(--card)}
  .week-head{display:flex;align-items:center;gap:14px;padding:16px 18px;cursor:pointer;user-select:none;
    background:linear-gradient(90deg,var(--wk,#333) 0%, transparent 120%);position:relative}
  .week-head .wk-no{width:44px;height:44px;border-radius:12px;display:grid;place-items:center;
    font-family:'Kanit';font-weight:800;font-size:18px;background:rgba(0,0,0,.28);color:#fff;flex:0 0 auto}
  .week-head .wk-meta{flex:1;min-width:0}
  .week-head .wk-meta h3{margin:0;font-size:18px}
  .week-head .wk-meta small{color:#eaf0ff;opacity:.85;font-size:12.5px}
  .week-head .wk-prog{font-size:12px;text-align:right;flex:0 0 auto}
  .week-head .wk-prog b{font-family:'Kanit';font-size:16px}
  .chev{transition:.3s;font-size:14px;opacity:.9}
  .week.open .chev{transform:rotate(180deg)}
  .week-body{display:none;padding:6px 14px 16px}
  .week.open .week-body{display:block;animation:fade .35s ease}
  @keyframes fade{from{opacity:0;transform:translateY(-6px)}to{opacity:1;transform:none}}
  .wk-bar{height:6px;background:#0e1626;border-radius:999px;overflow:hidden;margin:0 4px 8px}
  .wk-bar>i{display:block;height:100%;width:0;background:var(--wk,#888);transition:width .5s}

  /* ---------- DAY CARD ---------- */
  .day{border:1px solid var(--line);border-radius:16px;margin:12px 4px;background:var(--bg2);overflow:hidden}
  .day.done{border-color:var(--green);box-shadow:0 0 0 1px var(--green) inset}
  .day-head{display:flex;align-items:flex-start;gap:12px;padding:15px 16px 12px}
  .day-no{width:40px;height:40px;flex:0 0 auto;border-radius:11px;display:grid;place-items:center;
    background:var(--card2);font-family:'Kanit';font-weight:700;border:1px solid var(--line)}
  .day.done .day-no{background:var(--green);color:#062b1a;border-color:var(--green)}
  .day.milestone .day-no{background:var(--gold);color:#3a2c00;border-color:var(--gold)}
  .day-title{flex:1;min-width:0}
  .day-title h4{margin:0;font-size:16.5px}
  .day-title .en{color:var(--muted);font-size:13px;font-weight:500}
  .day-title .goal{font-size:13px;margin-top:5px;color:#cdd8f0}
  .day-title .goal b{color:var(--accent)}
  .skill-tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:8px}
  .tag{font-size:11px;padding:3px 9px;border-radius:999px;font-weight:600;border:1px solid transparent}
  .tag.L{background:rgba(77,163,255,.15);color:#8fc4ff;border-color:#2f5c8a}
  .tag.R{background:rgba(165,94,234,.15);color:#c89bff;border-color:#5c3f8a}
  .tag.G{background:rgba(0,210,168,.13);color:#5fe6c8;border-color:#1c6b5a}
  .tag.V{background:rgba(255,159,67,.15);color:#ffc48a;border-color:#8a5c2a}
  .tag.S{background:rgba(253,121,168,.15);color:#ff9dc4;border-color:#8a3f5f}
  .tag.W{background:rgba(95,107,255,.15);color:#a6adff;border-color:#3f478a}
  .tag.RV{background:rgba(255,210,63,.13);color:#ffe08a;border-color:#8a7420}
  .tag.M{background:var(--gold);color:#3a2c00;border-color:var(--gold)}
  .day-time{margin-left:auto;font-size:12px;color:var(--muted);white-space:nowrap;padding-top:3px}
  .day-time b{color:var(--gold);font-family:'Kanit'}

  .day-body{padding:0 16px 14px 68px}
  @media(max-width:600px){.day-body{padding-left:16px}}
  .block{display:flex;gap:10px;font-size:13px;padding:5px 0;border-bottom:1px dashed var(--line)}
  .block:last-child{border-bottom:none}
  .block .tm{flex:0 0 74px;color:var(--gold);font-weight:600;font-size:12px}
  .block .ac small{color:var(--muted);display:block;font-size:11.5px}
  .schedule-title,.tasks-title,.game-title{font-family:'Kanit';font-weight:600;font-size:13.5px;
    margin:14px 0 6px;color:#dfe7fb;text-transform:uppercase;letter-spacing:.5px;opacity:.9}

  .task{display:flex;gap:10px;align-items:flex-start;padding:7px 10px;border-radius:10px;cursor:pointer;
    transition:background .15s}
  .task:hover{background:var(--card2)}
  .task input{appearance:none;width:20px;height:20px;border:2px solid var(--line);border-radius:6px;
    flex:0 0 auto;margin-top:2px;cursor:pointer;position:relative;transition:.15s;background:var(--bg)}
  .task input:checked{background:var(--green);border-color:var(--green)}
  .task input:checked:after{content:"✓";position:absolute;color:#062b1a;font-weight:800;font-size:13px;
    top:-1px;left:3px}
  .task label{font-size:13.5px;cursor:pointer;flex:1}
  .task input:checked + label{color:var(--muted);text-decoration:line-through}

  .game{background:linear-gradient(135deg,rgba(38,222,129,.10),rgba(108,92,231,.10));
    border:1px dashed var(--accent);border-radius:12px;padding:11px 14px;margin-top:10px;font-size:13px}
  .game .g-name{font-family:'Kanit';font-weight:600;color:var(--accent);display:flex;align-items:center;gap:7px}
  .game .g-desc{margin-top:3px;color:#d6e0f5}
  .game a{font-size:12px}
  .tipbox{background:rgba(255,210,63,.08);border:1px solid #6b5a1e;border-radius:12px;
    padding:10px 14px;margin-top:10px;font-size:12.8px;color:#ffe6a3}
  .tipbox b{color:var(--gold)}

  /* ---------- GAMES MASTER ---------- */
  .games-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
  @media(max-width:820px){.games-grid{grid-template-columns:1fr}}
  .gcard{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px}
  .gcard h4{margin:0 0 4px;font-size:15px;display:flex;align-items:center;gap:8px}
  .gcard .for{font-size:11.5px;color:var(--accent);font-weight:600;margin-bottom:8px}
  .gcard p{font-size:12.8px;color:#cdd8f0;margin:0 0 8px}
  .gcard .tool{font-size:12px;padding:3px 0;color:var(--muted)}
  .gcard .tool b{color:var(--ink)}

  /* ---------- EXAM CHECKLIST ---------- */
  .exam{background:linear-gradient(135deg,rgba(255,210,63,.10),rgba(255,107,107,.08));
    border:1px solid #6b5a1e;border-radius:var(--radius);padding:22px}
  .exam ul{list-style:none;padding:0;margin:10px 0 0}
  .exam li{padding:8px 0;border-bottom:1px dashed var(--line);font-size:14px;display:flex;gap:10px}
  .exam li:before{content:"✅"}

  /* ---------- FOOTER ---------- */
  .foot{display:flex;flex-wrap:wrap;gap:12px;justify-content:space-between;align-items:center;
    margin-top:30px;padding-top:20px;border-top:1px solid var(--line);color:var(--muted);font-size:13px}
  .btn{font-family:'Kanit';font-weight:600;border:none;border-radius:12px;padding:10px 18px;cursor:pointer;
    font-size:13.5px}
  .btn.ghost{background:transparent;border:1px solid var(--line);color:var(--muted)}
  .btn.ghost:hover{border-color:var(--hot);color:var(--hot)}
  .btn.solid{background:linear-gradient(135deg,var(--brand),var(--brand2));color:#fff}
  .toast{position:fixed;left:50%;bottom:26px;transform:translateX(-50%) translateY(80px);
    background:var(--card);border:1px solid var(--gold);color:var(--gold);padding:13px 22px;border-radius:14px;
    font-family:'Kanit';font-weight:600;box-shadow:var(--shadow);opacity:0;transition:.4s;z-index:99;font-size:14px}
  .toast.show{transform:translateX(-50%) translateY(0);opacity:1}
  .mini-legend{display:flex;flex-wrap:wrap;gap:8px;margin-top:8px}
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <header class="hero">
    <span class="badge-teacher">🎓 คอร์สจากครูติวเตอร์ 30 ปี · Coached by a 30-yr master tutor</span>
    <h1>TOEIC 60 วัน พิชิตเป้า 🚀<br>Your 2-Month TOEIC Quest</h1>
    <p class="sub">แผนติวครบ 4 ทักษะ (ฟัง–อ่าน–พูด–เขียน) · 5 วัน/สัปดาห์ · วันละ 2–4 ชม. · เก็บ XP เลื่อนแรงก์ ปลดล็อกเหรียญตรา ไม่มีเบื่อ!</p>
    <p class="sub">Full 4-skill plan (L·R·S·W) · 5 days/week · 2–4 hrs/day · Earn XP, rank up, unlock badges — learning that never gets boring.</p>
    <div class="quote" id="quote">"เก่งไม่ได้มาจากพรสวรรค์ แต่มาจากการซ้อมที่สนุกทุกวัน" — ครูของเธอ 💪</div>
  </header>

  <!-- DASHBOARD -->
  <div class="dash">
    <div class="card">
      <div class="lvl-top">
        <div class="rank">
          <div class="ring" id="ring"><span id="rankEmoji">🐣</span></div>
          <div>
            <div class="name" id="rankName">มือใหม่หัดขับ<small id="rankNameEn">Rookie · Level 1</small></div>
          </div>
        </div>
        <div class="xp-num"><b id="xpNow">0</b><small>XP · เป้าเลเวลถัดไป <span id="xpNext">350</span></small></div>
      </div>
      <div class="bar"><i id="xpBar"></i></div>
      <div class="bar-label"><span>Level ปัจจุบัน</span><span id="xpToGo">อีก 350 XP เลื่อนแรงก์</span></div>
    </div>

    <div class="card">
      <div class="stats">
        <div class="stat pct"><b id="stPct">0%</b><small>คืบหน้าทั้งคอร์ส / Progress</small></div>
        <div class="stat days"><b id="stDays">0<span style="font-size:14px;color:var(--muted)">/40</span></b><small>วันที่เรียนจบ / Days done</small></div>
        <div class="stat streak"><b id="stStreak">0 🔥</b><small>สตรีคต่อเนื่อง / Day streak</small></div>
        <div class="stat tasks"><b id="stTasks">0</b><small>ภารกิจสำเร็จ / Tasks done</small></div>
      </div>
    </div>
  </div>

  <!-- ACHIEVEMENTS -->
  <div class="ach-wrap">
    <div class="section-title"><h2>🏅 เหรียญตรา / Achievements</h2><span class="line"></span></div>
    <div class="badges" id="badges"></div>
  </div>

  <!-- INFO -->
  <div class="section-title"><h2>🧭 เริ่มยังไงดี / How to start</h2><span class="line"></span></div>
  <div class="info-grid">
    <div class="card info">
      <h3>📋 กติกาเก็บ XP / How XP works</h3>
      <ul>
        <li>ทำภารกิจ (ติ๊ก checklist) สำเร็จ 1 ข้อ = <b>+10 XP</b></li>
        <li>เรียนจบครบทั้งวัน = โบนัส <b>+40 XP</b> 🎉</li>
        <li>สะสม XP เลื่อนจาก <b>มือใหม่ → ตำนาน 900+</b> รวม 8 แรงก์</li>
        <li>เข้าเรียนต่อเนื่องทุกวันเพื่อสะสม <b>สตรีค 🔥</b></li>
        <li>ความคืบหน้าถูกบันทึกอัตโนมัติในเครื่องคุณ (ปิดแล้วเปิดใหม่ก็ยังอยู่)</li>
      </ul>
    </div>
    <div class="card info">
      <h3>🎯 ก่อนเริ่ม Day 1 / Before you start</h3>
      <ul>
        <li><b>ประเมินระดับ:</b> Day 1 คือ diagnostic test — ทำเพื่อ "รู้จุดสตาร์ท" ไม่ต้องกังวลคะแนน</li>
        <li><b>ปรับความยากเอง:</b> ถ้า diagnostic &lt; 400 เน้นทำ task พื้นฐานให้ครบก่อน; ถ้า &gt; 650 เพิ่มโจทย์จับเวลาและ S&amp;W มากขึ้น</li>
        <li><b>เตรียมของ:</b> สมุด error-log, แอปทำ flashcard, หูฟัง, และไมค์สำหรับอัดเสียงพูด</li>
        <li><b>ตั้งวันสอบจริง</b> แล้วนับถอยหลัง 60 วันจากวันนี้</li>
      </ul>
      <div class="pill-row">
        <span class="pill">🎧 Listening 45 นาที · 100 ข้อ</span>
        <span class="pill">📖 Reading 75 นาที · 100 ข้อ</span>
        <span class="pill">🗣️ Speaking 11 ข้อ</span>
        <span class="pill">✏️ Writing 8 ข้อ</span>
      </div>
    </div>
  </div>

  <!-- WEEKS -->
  <div class="section-title"><h2>📅 ตารางเรียน 8 สัปดาห์ / 8-Week Schedule</h2><span class="line"></span></div>
  <div id="weeks"></div>

  <!-- GAMES MASTER -->
  <div class="section-title"><h2>🎮 คลังเกม & แอปฝึกทักษะ / Game & App Arsenal</h2><span class="line"></span></div>
  <p style="color:var(--muted);font-size:14px;margin-top:-4px">เล่นหลังเรียนจบเพื่อทดสอบว่า "เข้าใจจริงไหม" — สนุกแต่ได้ฝึกของจริง / Play after each lesson to test if it really stuck.</p>
  <div class="games-grid" id="gamesMaster"></div>

  <!-- EXAM CHECKLIST -->
  <div class="section-title"><h2>🎒 เช็กลิสต์วันสอบจริง / Exam-Day Checklist</h2><span class="line"></span></div>
  <div class="exam">
    <p style="margin:0;font-size:14px">ทำ 2–3 วันก่อนสอบและเช้าวันสอบ / Do this 2–3 days before and on the morning of the test:</p>
    <ul>
      <li>เตรียมบัตรประชาชน/พาสปอร์ต + เอกสารยืนยันการสมัคร (Bring ID + registration)</li>
      <li>รู้เส้นทางและเวลาไปสนามสอบ เผื่อเวลา 30 นาที (Know the route, arrive early)</li>
      <li>นอนให้พอ 7–8 ชม. คืนก่อนสอบ — อย่าอ่านหนักดึก (Sleep well, no cramming)</li>
      <li>เช้าวันสอบ: warm-up หู 10 นาทีด้วยคลิปภาษาอังกฤษ (Warm up your ears)</li>
      <li>อ่าน error-log สรุปกับดักที่เคยพลาดรอบสุดท้าย (Review your trap notes)</li>
      <li>กลยุทธ์เวลา Reading: ห้ามติดข้อเดียวเกิน 1 นาที เดาแล้วมาร์กไว้ (Never stall &gt;1 min)</li>
      <li>ตอบให้ครบทุกข้อ — TOEIC ไม่หักคะแนนข้อผิด (Answer every question!)</li>
    </ul>
  </div>

  <!-- FOOTER -->
  <div class="foot">
    <span>© แผนติว TOEIC ออกแบบเฉพาะคุณ · ปิด-เปิดไฟล์นี้ได้เรื่อยๆ ความคืบหน้าไม่หาย 💾</span>
    <button class="btn ghost" id="resetBtn">↺ ล้างความคืบหน้าทั้งหมด / Reset</button>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
/* ============================================================
   CURRICULUM DATA — 8 weeks x 5 days = 40 study days
   ============================================================ */
const RANKS = [
  {min:0,    emoji:"🐣", th:"มือใหม่หัดขับ",       en:"Rookie"},
  {min:350,  emoji:"📚", th:"นักเรียนขยัน",        en:"Diligent Learner"},
  {min:750,  emoji:"⚔️", th:"จอมยุทธ์ไวยากรณ์",   en:"Grammar Warrior"},
  {min:1150, emoji:"🎧", th:"เซียนฟังจับใจความ",   en:"Listening Ninja"},
  {min:1600, emoji:"⚡", th:"นักอ่านสายฟ้า",       en:"Speed Reader"},
  {min:2050, emoji:"👑", th:"ราชานักพูด-นักเขียน",  en:"Speak & Write Royalty"},
  {min:2500, emoji:"🧙", th:"ปรมาจารย์ TOEIC",      en:"TOEIC Grandmaster"},
  {min:2950, emoji:"🏆", th:"ตำนาน 900+",           en:"Legend 900+"}
];

const GAMES_MASTER = [
  {em:"🔤",for:"คำศัพท์ / Vocabulary",name:"Quizlet + Freerice",
   desc:"สร้างชุดคำศัพท์เอง เล่นโหมด Match/Gravity แข่งเวลา; Freerice ตอบศัพท์บริจาคข้าวไปด้วย",
   tools:["Quizlet — flashcard & mini-games","Freerice.com — vocab quiz เพื่อการกุศล","Memrise — จำศัพท์ด้วยภาพ"]},
  {em:"🎧",for:"การฟัง / Listening",name:"Listening Labs & Shadowing",
   desc:"ฟังบทสนทนาสั้นแล้วตอบ quiz แล้วพูดตาม (shadowing) เพื่อจับสำเนียงและความเร็ว",
   tools:["Randall's ESL Cyber Listening Lab","BBC Learning English — 6 Minute English","YouTube: เปิดซับ แล้ว shadow ตาม"]},
  {em:"⚔️",for:"ไวยากรณ์ / Grammar",name:"Kahoot & Quizizz",
   desc:"ค้นควิซ TOEIC Grammar/Part 5 เล่นแข่งกับเวลา เก็บแต้ม สนุกเหมือนเกมโชว์",
   tools:["Kahoot! — ค้น 'TOEIC Part 5'","Quizizz — quiz แข่งขัน","British Council LearnEnglish — grammar games"]},
  {em:"🗣️",for:"การพูด / Speaking",name:"ELSA Speak & Language Exchange",
   desc:"ฝึกออกเสียงให้แอปให้คะแนนแบบเรียลไทม์ แล้วคุยจริงกับเจ้าของภาษา",
   tools:["ELSA Speak — คะแนนออกเสียงรายคำ","HelloTalk / Tandem — คุยกับเจ้าของภาษา","อัดเสียงตัวเองตอบโจทย์ Speaking แล้วฟังซ้ำ"]},
  {em:"⚡",for:"การอ่าน / Reading",name:"Speed-Reading Sprint",
   desc:"อ่านข่าวสั้นภาษาอังกฤษจับเวลา ตอบ 3 คำถามใจความ ฝึก skim & scan ให้ไว",
   tools:["BBC / CNN 10 — ข่าวสั้น","News in Levels — ข่าวแบ่งระดับ","จับเวลา Part 7 ด้วยนาฬิกาจับเวลา"]},
  {em:"✏️",for:"การเขียน / Writing",name:"Journal + Grammarly Check",
   desc:"เขียนความเห็น 5–7 ประโยคทุกวัน ให้ Grammarly ตรวจ แล้วแก้ที่ผิดซ้ำ",
   tools:["Grammarly — ตรวจไวยากรณ์อัตโนมัติ","เขียน daily journal สั้นๆ","เลียนแบบโครงเรียงความ opinion (intro-body-conclusion)"]}
];

/* Each day: id, day#, th title, en title, skills[], goal, time, schedule[{tm,ac,acEn}], tasks[], game{name,desc,url}, tip, milestone */
const WEEKS = [
{n:1, color:"var(--teal)", th:"รู้เขารู้เรา: วางรากฐาน", en:"Know the Test, Build the Base", days:[
  {id:"d1", day:1, th:"วันประเมินตัวเอง", en:"Diagnostic Day", skills:["M","RV"], time:"2.5 ชม.",
   goal:"รู้ระดับตัวเองจริง และตั้งเป้าที่วัดผลได้ / Find your real level & set a measurable goal.",
   schedule:[
     {tm:"20 นาที",ac:"ทำความรู้จักข้อสอบ TOEIC ทั้ง 7 พาร์ท L&R + S&W",acEn:"Learn the full test format"},
     {tm:"90 นาที",ac:"ทำ diagnostic mock test จับเวลาจริง",acEn:"Take a timed diagnostic test"},
     {tm:"30 นาที",ac:"ตรวจคะแนน + จดจุดอ่อน 3 อันดับ",acEn:"Score & log top-3 weak parts"},
     {tm:"20 นาที",ac:"ตั้งเป้าคะแนน + เขียนสัญญาใจแปะไว้",acEn:"Set target & write a commitment note"}],
   tasks:["ดูสรุปโครงสร้างข้อสอบ TOEIC ทั้ง 7 พาร์ท (L&R) + ส่วน Speaking & Writing",
     "ทำ diagnostic test 1 ชุด จับเวลาแบบสนามจริง",
     "บันทึกคะแนน Listening / Reading แยกกัน ลงสมุด",
     "ทำ error-log: จดพาร์ทที่ผิดเยอะที่สุด 3 อันดับ",
     "เขียนเป้าหมายคะแนน + วันสอบจริง แล้วแปะไว้หน้าโต๊ะ"],
   game:{name:"Freerice",desc:"ตอบคำศัพท์อังกฤษ ยิ่งถูกยิ่งบริจาคข้าว — วอร์มคลังศัพท์แบบไม่กดดัน",url:"freerice.com"},
   tip:"อย่ากลัวคะแนน diagnostic ต่ำ มันคือ 'จุดสตาร์ท' ไม่ใช่ 'คำตัดสิน' — 60 วันเปลี่ยนได้เยอะมาก!"},
  {id:"d2", day:2, th:"ไวยากรณ์แกนกลาง: ชนิดของคำ", en:"Grammar Core: Parts of Speech", skills:["G","R"], time:"2.5 ชม.",
   goal:"ตอบ Part 5 ได้จาก 'ตำแหน่งคำ' โดยไม่ต้องแปลทั้งประโยค / Answer Part 5 by word position.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน error-log เมื่อวาน",acEn:"Review yesterday's errors"},
     {tm:"70 นาที",ac:"เรียน 8 ชนิดของคำ + คำลงท้ายที่บอกชนิดคำ",acEn:"8 parts of speech + suffix clues"},
     {tm:"45 นาที",ac:"ฝึก Part 5 (word form) 20 ข้อ",acEn:"Practice 20 Part 5 word-form items"},
     {tm:"20 นาที",ac:"เกม + จดสรุป",acEn:"Game + notes"}],
   tasks:["เรียน noun/verb/adjective/adverb + คำลงท้าย (-tion, -ly, -ous, -ment)",
     "ฝึก Part 5 แนว word-form 20 ข้อ",
     "จดศัพท์ใหม่ 10 คำ พร้อมระบุชนิดคำ ลง flashcard",
     "อธิบายเหตุผลของข้อที่ผิดทุกข้อ (ห้ามข้าม)"],
   game:{name:"Quizlet Match",desc:"สร้างชุดศัพท์วันนี้แล้วเล่นเกมจับคู่ จับเวลาให้เร็วขึ้นทุกครั้ง",url:"quizlet.com"},
   tip:"~90% ของ Part 5 ตอบได้จากตำแหน่งคำ ถ้าเห็นช่องว่างหลัง 'the' ให้คิดถึงคำนามก่อน"},
  {id:"d3", day:3, th:"Listening Part 1: รูปภาพ", en:"Listening Part 1: Photographs", skills:["L","V"], time:"2.5 ชม.",
   goal:"ดักกับดักคำพ้องเสียง และเลือกประโยคที่ตรงภาพที่สุด / Beat sound-alike traps.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน flashcard เมื่อวาน",acEn:"Flashcard review"},
     {tm:"60 นาที",ac:"เทคนิค Part 1: subject/action/tense + กับดัก",acEn:"Part 1 technique + traps"},
     {tm:"45 นาที",ac:"ฝึก Part 1 (12 ภาพ) + Part 2 อุ่นเครื่อง",acEn:"Practice 12 photos + warm Part 2"},
     {tm:"30 นาที",ac:"Shadowing เสียงเจ้าของภาษา",acEn:"Shadowing native audio"}],
   tasks:["เรียนกับดัก Part 1: คำพ้องเสียง, passive vs active, คำที่ไม่ตรงภาพ",
     "ฝึก Part 1 อย่างน้อย 12 ภาพ พร้อมฟังเฉลย",
     "Shadowing 10 ประโยคจากเฉลย ออกเสียงตามให้ทัน",
     "จดศัพท์หมวดออฟฟิศ/สถานที่ทำงาน 15 คำ"],
   game:{name:"Randall's ESL Listening Lab",desc:"ฟังคลิปสั้นแล้วทำ quiz เช็กความเข้าใจทันที",url:"esl-lab.com"},
   tip:"Part 1 ให้ฟัง 'กริยา + tense' เป็นหลัก ภาพคนกำลังทำอะไร มักตอบด้วย present continuous"},
  {id:"d4", day:4, th:"Listening Part 2: ถาม–ตอบ", en:"Listening Part 2: Question-Response", skills:["L"], time:"2.5 ชม.",
   goal:"จับ WH-word แรกให้ได้ และเลี่ยงกับดักคำซ้ำ / Catch the first WH-word, dodge repeat-word traps.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหูด้วยคลิปสั้น",acEn:"Ear warm-up"},
     {tm:"65 นาที",ac:"เทคนิคแยกประเภทคำถาม WH / Yes-No / Tag",acEn:"Question types"},
     {tm:"50 นาที",ac:"ฝึก Part 2 25 ข้อ",acEn:"Practice 25 Part 2 items"},
     {tm:"20 นาที",ac:"เกม + จดประเภทที่พลาดบ่อย",acEn:"Game + error notes"}],
   tasks:["เรียนวิธีล็อกคำถามจาก WH-word แรก (Who/Where/When/Why/How)",
     "เรียนกับดัก: คำซ้ำ, homonym, คำตอบอ้อม (indirect answers)",
     "ฝึก Part 2 จำนวน 25 ข้อ",
     "จดประเภทคำถามที่พลาดบ่อยลง error-log"],
   game:{name:"Kahoot! (TOEIC Part 2)",desc:"เล่นควิซถาม-ตอบแข่งเวลา ฝึกตัดสินใจเร็ว",url:"kahoot.com"},
   tip:"ถ้าได้ยินคำซ้ำกับในคำถามเป๊ะๆ ให้ 'ระวัง' — มักเป็นกับดัก ไม่ใช่คำตอบ"},
  {id:"d5", day:5, th:"รีวิวสัปดาห์ 1 + Tenses", en:"Week 1 Review + Verb Tenses", skills:["G","RV"], time:"2 ชม.",
   goal:"ปิดจุดอ่อนสัปดาห์แรก และแม่นสัญญาณคำบอกเวลา / Lock in week 1 & tense signal words.",
   schedule:[
     {tm:"40 นาที",ac:"ทบทวน 12 tenses + สัญญาณเวลา",acEn:"12 tenses + time signals"},
     {tm:"35 นาที",ac:"ฝึก Part 5 (tense) 15 ข้อ",acEn:"15 tense items"},
     {tm:"25 นาที",ac:"mini-quiz รวมทุกอย่างสัปดาห์นี้ 20 ข้อ",acEn:"20-item weekly quiz"},
     {tm:"20 นาที",ac:"วันเล่นเกม! ปลดปล่อยความสนุก",acEn:"Game day — have fun!"}],
   tasks:["ทบทวน 12 tenses หลัก + คำบอกเวลา (already, since, ago, by, for)",
     "ฝึก Part 5 แนว tense 15 ข้อ",
     "ทบทวน flashcard ทั้งสัปดาห์ (60+ คำ)",
     "ทำ mini-quiz 20 ข้อ รวมทุกเรื่องของสัปดาห์ 1"],
   game:{name:"Quizlet Live / Gravity + คลิปครูสอน",desc:"เล่นเกมศัพท์แนวแข่งขัน แล้วดูคลิปครู TOEIC 1 คลิปปิดสัปดาห์",url:"quizlet.com"},
   tip:"รางวัลตัวเองเมื่อจบสัปดาห์แรก! สมองจำการเรียนที่มีความสุขได้ดีกว่าเสมอ"}
]},
{n:2, color:"var(--blue)", th:"จับใจความเสียง", en:"Master the Audio", days:[
  {id:"d6", day:6, th:"Listening Part 3: บทสนทนา", en:"Part 3: Conversations", skills:["L"], time:"3 ชม.",
   goal:"อ่านคำถามล่วงหน้า แล้วฟังเก็บ who/what/where / Preview questions, then listen for key info.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหู + ทบทวน",acEn:"Warm-up"},
     {tm:"75 นาที",ac:"เทคนิค 'อ่านคำถามก่อนฟัง' + จับ 3W",acEn:"Preview-then-listen strategy"},
     {tm:"60 นาที",ac:"ฝึก Part 3 3 ชุด (9 คำถาม)",acEn:"Practice 3 conversation sets"},
     {tm:"30 นาที",ac:"Shadowing + เกม",acEn:"Shadowing + game"}],
   tasks:["เรียนเทคนิคอ่าน 3 คำถามล่วงหน้าใน 8 วินาที",
     "ฝึกจับ who's talking / what about / what next",
     "ฝึก Part 3 อย่างน้อย 3 บทสนทนา",
     "Shadowing 1 บทสนทนาเต็ม เลียนเสียงและจังหวะ"],
   game:{name:"BBC 6 Minute English",desc:"ฟังบทสนทนา 6 นาทีพร้อมสคริปต์ ฝึกจับใจความบทยาว",url:"bbc.co.uk/learningenglish"},
   tip:"อย่าฟังเพื่อ 'แปลทุกคำ' — ฟังเพื่อ 'จับใจความ' คำถามชี้เป้าให้แล้วว่าต้องฟังอะไร"},
  {id:"d7", day:7, th:"ไวยากรณ์: ประธาน–กริยา & โครงสร้าง", en:"Grammar: Agreement & Structure", skills:["G","R"], time:"2.5 ชม.",
   goal:"แม่นเรื่องเอกพจน์/พหูพจน์ และโครงสร้างประโยคซับซ้อน / Nail agreement & clauses.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"70 นาที",ac:"subject-verb agreement + relative clauses",acEn:"Agreement + clauses"},
     {tm:"45 นาที",ac:"ฝึก Part 5/6 20 ข้อ",acEn:"20 items"},
     {tm:"20 นาที",ac:"เกม + จดสรุป",acEn:"Game + notes"}],
   tasks:["เรียน subject-verb agreement (each, every, everyone = เอกพจน์)",
     "เรียน relative clauses (who/which/that/whose)",
     "ฝึก Part 5 & 6 รวม 20 ข้อ",
     "จดโครงสร้างที่ผิดบ่อยลง error-log"],
   game:{name:"Quizizz (Grammar)",desc:"ควิซไวยากรณ์แข่งขัน มีมีมและแต้มคอมโบ สนุกไม่ง่วง",url:"quizizz.com"},
   tip:"เจอ 'a number of' = พหูพจน์, 'the number of' = เอกพจน์ — จุดนี้ TOEIC ชอบออก"},
  {id:"d8", day:8, th:"Listening Part 4: บทพูด/ประกาศ", en:"Part 4: Talks & Announcements", skills:["L"], time:"3 ชม.",
   goal:"จับโครงบทพูด (จุดประสงค์–รายละเอียด–สิ่งที่จะเกิด) / Track talk structure.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหู",acEn:"Warm-up"},
     {tm:"75 นาที",ac:"ประเภทบทพูด: ประกาศ, ข้อความเสียง, โฆษณา",acEn:"Talk types"},
     {tm:"60 นาที",ac:"ฝึก Part 4 3 ชุด",acEn:"Practice 3 talk sets"},
     {tm:"30 นาที",ac:"Shadowing + เกม",acEn:"Shadowing + game"}],
   tasks:["เรียนโครงบทพูด: purpose → details → next step",
     "ฝึกจับคำถามแนว 'What will the listener probably do next?'",
     "ฝึก Part 4 อย่างน้อย 3 บทพูด",
     "Shadowing 1 ประกาศ เลียนน้ำเสียงและการเน้นคำ"],
   game:{name:"TED-Ed / YouTube (ซับ EN)",desc:"ฟังบทพูดสั้นเปิดซับอังกฤษ แล้วสรุปใจความ 2 ประโยค",url:"ed.ted.com"},
   tip:"คำถามข้อสุดท้ายของแต่ละชุดมักอยู่ 'ท้ายบทพูด' — เตรียมหูให้พร้อมตอนใกล้จบ"},
  {id:"d9", day:9, th:"ศัพท์เดินทาง/โรงแรม + ทวน Part 2", en:"Travel/Hotel Vocab + Part 2 Recycle", skills:["V","L"], time:"2.5 ชม.",
   goal:"เพิ่มคลังศัพท์หมวดฮิต และรีไซเคิลจุดอ่อน Part 2 / Grow themed vocab.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"60 นาที",ac:"ศัพท์หมวด travel/hotel/restaurant 25 คำ",acEn:"25 themed words"},
     {tm:"50 นาที",ac:"ฝึก Part 2 25 ข้อ เน้นประเภทที่เคยพลาด",acEn:"Part 2 targeted practice"},
     {tm:"25 นาที",ac:"เกมศัพท์",acEn:"Vocab game"}],
   tasks:["เรียนศัพท์ travel/hotel/restaurant 25 คำ พร้อมประโยคตัวอย่าง",
     "ทำ flashcard ศัพท์ใหม่ทั้งหมด",
     "ฝึก Part 2 อีก 25 ข้อ เจาะประเภทที่พลาดบ่อย",
     "เขียนประโยคของตัวเอง 5 ประโยคจากศัพท์ใหม่"],
   game:{name:"Memrise / Quizlet Gravity",desc:"จำศัพท์หมวดเดินทางด้วยภาพและเกมพิมพ์แข่งเวลา",url:"memrise.com"},
   tip:"เรียนศัพท์เป็น 'หมวด' จำง่ายกว่าเรียนคำโดดๆ เพราะสมองผูกเป็นเรื่องราว"},
  {id:"d10", day:10, th:"รีวิวสัปดาห์ 2 + Listening mini-test", en:"Week 2 Review + Mini Listening Test", skills:["L","RV"], time:"2.5 ชม.",
   goal:"วัดพัฒนาการฟัง Part 1–4 รวดเดียว / Measure full Listening progress.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหู",acEn:"Warm-up"},
     {tm:"50 นาที",ac:"ทำ Listening mini-test (Part 1–4) จับเวลา",acEn:"Timed listening mini-test"},
     {tm:"40 นาที",ac:"ตรวจ + ฟังซ้ำข้อที่ผิด",acEn:"Review wrong answers"},
     {tm:"25 นาที",ac:"วันเล่นเกม!",acEn:"Game day!"}],
   tasks:["ทำ Listening mini-test ครบ Part 1–4 จับเวลาจริง",
     "เทียบคะแนนกับ diagnostic — ดีขึ้นกี่ข้อ?",
     "ฟังซ้ำทุกข้อที่ผิด อ่าน transcript ประกอบ",
     "อัปเดต error-log จุดอ่อนที่เหลือ"],
   game:{name:"วันเล่นเกมรวม",desc:"เลือกเกมที่ชอบที่สุดจากคลังเกมด้านล่าง เล่นให้เต็มที่ 30 นาที",url:""},
   tip:"เห็นตัวเลขพัฒนาการชัดๆ คือเชื้อเพลิงชั้นดี — จดไว้ว่าคุณเก่งขึ้นแล้วจริงๆ!"}
]},
{n:3, color:"var(--purple)", th:"ถอดรหัสการอ่าน", en:"Crack the Reading", days:[
  {id:"d11", day:11, th:"Part 5 เจาะลึก: บุพบท & คำเชื่อม", en:"Part 5 Deep: Prepositions & Conjunctions", skills:["G","R"], time:"3 ชม.",
   goal:"แยก in/on/at/by และ because/although/despite ให้ขาด / Master prepositions & connectors.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"80 นาที",ac:"บุพบทเวลา/สถานที่ + คำเชื่อม (although/despite/because of)",acEn:"Prepositions + connectors"},
     {tm:"60 นาที",ac:"ฝึก Part 5 25 ข้อ",acEn:"25 items"},
     {tm:"25 นาที",ac:"เกม + จดสรุป",acEn:"Game + notes"}],
   tasks:["เรียนบุพบทเวลา/สถานที่ (in/on/at/by/until/within)",
     "เรียนคำเชื่อม: although vs despite, because vs because of",
     "ฝึก Part 5 25 ข้อเน้นบุพบท+คำเชื่อม",
     "จดคู่คำที่สับสนบ่อยลง flashcard"],
   game:{name:"British Council Grammar Games",desc:"เกมไวยากรณ์ฟรีจาก British Council เจาะบุพบทและคำเชื่อม",url:"learnenglish.britishcouncil.org"},
   tip:"'despite/in spite of' ตามด้วยคำนาม; 'although/though' ตามด้วยประโยค — TOEIC ออกบ่อยมาก"},
  {id:"d12", day:12, th:"Part 6: เติมข้อความ", en:"Part 6: Text Completion", skills:["R","G"], time:"3 ชม.",
   goal:"เลือกคำ/ประโยคให้เข้ากับบริบทย่อหน้า / Fill words & a sentence by context.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"70 นาที",ac:"เทคนิค Part 6 + การเติมประโยค (sentence insertion)",acEn:"Part 6 technique"},
     {tm:"65 นาที",ac:"ฝึก Part 6 4 ชุด",acEn:"Practice 4 passages"},
     {tm:"30 นาที",ac:"เกม + จดสรุป",acEn:"Game + notes"}],
   tasks:["เรียนวิธีอ่านทั้งย่อหน้าเพื่อเลือกคำที่เข้ากับบริบท",
     "เรียนการเติมประโยค (ดู discourse markers: however, therefore)",
     "ฝึก Part 6 อย่างน้อย 4 ชุด",
     "จดคำเชื่อมย่อหน้า (transition words) 15 คำ"],
   game:{name:"News in Levels",desc:"อ่านข่าวสั้นแบ่งระดับ ฝึกจับบริบทย่อหน้าแบบเบาๆ",url:"newsinlevels.com"},
   tip:"ข้อเติมประโยคใน Part 6 ให้ดู 'ประโยคก่อนและหลัง' ช่องว่างเสมอ อย่าดูเฉพาะช่องว่าง"},
  {id:"d13", day:13, th:"Part 7: บทความเดี่ยว", en:"Part 7: Single Passages", skills:["R"], time:"3 ชม.",
   goal:"อ่านอีเมล/ประกาศ/โฆษณา แล้วตอบแบบ skim & scan / Read & scan single texts fast.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"70 นาที",ac:"ประเภทบทความ + เทคนิค skim/scan + คำถาม detail/inference",acEn:"Passage types + skim/scan"},
     {tm:"70 นาที",ac:"ฝึก Part 7 single 5–6 บทความ จับเวลา",acEn:"Practice 5-6 passages (timed)"},
     {tm:"25 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนประเภทบทความ: email, notice, advertisement, article",
     "เรียนแยกคำถาม detail / inference / vocabulary-in-context",
     "ฝึก Part 7 single passage 5–6 บทความ จับเวลา",
     "จับเวลาเฉลี่ยต่อบทความ — ตั้งเป้าลดลงเรื่อยๆ"],
   game:{name:"Reading Sprint (BBC/CNN 10)",desc:"อ่านข่าวสั้น 1 ชิ้นใน 2 นาที แล้วตอบ 3 คำถามใจความให้ตัวเอง",url:"bbc.com/news"},
   tip:"อ่านคำถามก่อน 'แล้วค่อยล่าคำตอบ' ในบทความ — ประหยัดเวลากว่าอ่านทุกคำตั้งแต่ต้น"},
  {id:"d14", day:14, th:"ศัพท์ธุรกิจ/การเงิน + ตระกูลคำ", en:"Business/Finance Vocab + Word Families", skills:["V","R"], time:"2.5 ชม.",
   goal:"รู้ศัพท์ธุรกิจที่ TOEIC ชอบออก และแปลงคำข้ามชนิด / Business vocab & word families.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"65 นาที",ac:"ศัพท์ธุรกิจ/การเงิน 30 คำ + word families",acEn:"30 business words + families"},
     {tm:"45 นาที",ac:"ฝึก Part 5 word-form 15 ข้อ",acEn:"15 word-form items"},
     {tm:"25 นาที",ac:"เกมศัพท์",acEn:"Vocab game"}],
   tasks:["เรียนศัพท์ธุรกิจ/การเงิน 30 คำ (invoice, revenue, warranty, refund...)",
     "ฝึก word families: succeed/success/successful/successfully",
     "ฝึก Part 5 word-form 15 ข้อ",
     "ทำ flashcard พร้อมประโยคตัวอย่างจากบริบทธุรกิจ"],
   game:{name:"Quizlet (Business Set)",desc:"สร้าง/ค้นชุดศัพท์ธุรกิจ เล่น Match แข่งเวลาเก็บสถิติ",url:"quizlet.com"},
   tip:"จำ 1 คำ = จำทั้งตระกูล เช่นรู้ 'analyze' ก็ต่อยอด analysis/analyst/analytical ได้ทันที"},
  {id:"d15", day:15, th:"รีวิวสัปดาห์ 3 + Part 5 speed sprint", en:"Week 3 Review + Part 5 Speed Sprint", skills:["R","RV"], time:"2.5 ชม.",
   goal:"ตอบ Part 5 ให้ได้ ~20 วินาที/ข้อ / Hit ~20 sec/question on Part 5.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์ม",acEn:"Warm-up"},
     {tm:"45 นาที",ac:"Part 5 speed sprint 30 ข้อ จับเวลา 10 นาที",acEn:"30-item timed sprint"},
     {tm:"45 นาที",ac:"ตรวจ + วิเคราะห์ที่ผิด",acEn:"Review & analyze"},
     {tm:"25 นาที",ac:"วันเล่นเกม!",acEn:"Game day!"}],
   tasks:["ทำ Part 5 speed sprint 30 ข้อ ภายใน 10 นาที",
     "วิเคราะห์: ผิดเพราะไวยากรณ์ หรือศัพท์?",
     "ทบทวน flashcard ทั้งสัปดาห์ (70+ คำ)",
     "ทำ mini-quiz reading 20 ข้อรวมสัปดาห์นี้"],
   game:{name:"เลือกเกมโปรด + คลิปครู",desc:"เล่นเกมที่ชอบ 20 นาที แล้วดูคลิปเทคนิค Reading 1 คลิป",url:""},
   tip:"Part 5 คือ 'แหล่งเก็บเวลา' — ยิ่งเร็ว ยิ่งมีเวลาเหลือไปทุ่มกับ Part 7 ที่ยากกว่า"}
]},
{n:4, color:"var(--orange)", th:"รวมพลัง + สอบซ้อม 1", en:"Integrate + Mock Test 1", days:[
  {id:"d16", day:16, th:"Part 3&4: คำถามอนุมาน + กราฟิก", en:"Part 3&4: Inference + Graphics", skills:["L"], time:"3 ชม.",
   goal:"ตอบคำถามที่ต้องตีความ และอ่านตาราง/กราฟประกอบเสียง / Inference & graphic questions.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหู",acEn:"Warm-up"},
     {tm:"75 นาที",ac:"คำถาม inference + graphic (ดูตาราง+ฟัง)",acEn:"Inference + graphic Qs"},
     {tm:"60 นาที",ac:"ฝึก Part 3&4 มีกราฟิก 4 ชุด",acEn:"Practice with graphics"},
     {tm:"30 นาที",ac:"Shadowing + เกม",acEn:"Shadowing + game"}],
   tasks:["เรียนคำถาม inference: 'What does the man imply?'",
     "ฝึกอ่าน graphic (ตาราง/ราคา/ตารางเวลา) พร้อมฟัง",
     "ฝึก Part 3&4 แนวกราฟิก 4 ชุด",
     "จดสำนวนบอกนัย (implication) ที่เจอบ่อย"],
   game:{name:"YouTube Listening (ซับ)",desc:"ดูคลิปสัมภาษณ์สั้น เดา 'นัย' ของผู้พูด แล้วเช็กกับซับ",url:"youtube.com"},
   tip:"ข้อกราฟิก: กวาดตาดูตารางก่อนเสียงเริ่ม รู้ว่าจะต้องจับ 'ข้อมูลไหน' มาแมตช์"},
  {id:"d17", day:17, th:"Part 7: บทความคู่/สามบทความ", en:"Part 7: Double & Triple Passages", skills:["R"], time:"3.5 ชม.",
   goal:"เชื่อมข้อมูลข้ามหลายบทความเพื่อตอบ / Connect info across texts.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์ม",acEn:"Warm-up"},
     {tm:"75 นาที",ac:"เทคนิค cross-reference + คำถามที่ต้องรวมข้อมูล",acEn:"Cross-reference technique"},
     {tm:"85 นาที",ac:"ฝึก double/triple passages 3 ชุด จับเวลา",acEn:"Practice multi-passage sets"},
     {tm:"25 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนเทคนิค cross-reference (คำตอบซ่อนในบทความที่ 2/3)",
     "ฝึกจับคำถามที่ต้องรวมข้อมูล 2 บทความ",
     "ฝึก double/triple passage 3 ชุด จับเวลา",
     "จดเวลาเฉลี่ยต่อชุด ตั้งเป้าให้ทันเวลาสอบ"],
   game:{name:"Reading Sprint (ยาวขึ้น)",desc:"อ่านบทความยาว 1 ชิ้น จับเวลา สรุปใจความ 3 ข้อ",url:"newsinlevels.com"},
   tip:"อ่านบทความแรกจบแล้วค่อยดูคำถาม; คำถามรวมข้อมูลมักมีคำว่า 'according to both...'"},
  {id:"d18", day:18, th:"Speaking เริ่มต้น: อ่านออกเสียง + บรรยายภาพ", en:"Speaking Intro: Read Aloud + Describe Picture", skills:["S"], time:"2.5 ชม.",
   goal:"ออกเสียงชัด เน้นคำถูก และบรรยายภาพเป็นระบบ / Clear pronunciation & structured description.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มปาก/ลิ้น",acEn:"Mouth warm-up"},
     {tm:"60 นาที",ac:"เทคนิค read-aloud (intonation, linking) + describe picture",acEn:"Read-aloud + picture"},
     {tm:"55 นาที",ac:"อัดเสียงตัวเองทำโจทย์ + ฟังซ้ำ",acEn:"Record & self-review"},
     {tm:"20 นาที",ac:"เกมออกเสียง",acEn:"Pronunciation game"}],
   tasks:["เรียนเทคนิค read-aloud: การเน้นคำ, การเชื่อมเสียง (linking)",
     "เรียนโครงบรรยายภาพ: ภาพรวม → คน → กิจกรรม → รายละเอียด",
     "อัดเสียงตัวเองทำ read-aloud 2 ข้อ + describe 1 ภาพ",
     "ฟังเสียงตัวเองซ้ำ จดจุดที่ออกเสียงผิด"],
   game:{name:"ELSA Speak",desc:"ฝึกออกเสียงรายคำ แอปให้คะแนนทันที ปรับจนได้คะแนนสูง",url:"elsaspeak.com"},
   tip:"บรรยายภาพให้พูดจาก 'ภาพรวม → รายละเอียด' เสมอ และใช้ present continuous เป็นหลัก"},
  {id:"d19", day:19, th:"Writing เริ่มต้น: ประโยคจากภาพ + ตอบอีเมล", en:"Writing Intro: Sentence from Picture + Email", skills:["W"], time:"2.5 ชม.",
   goal:"เขียนประโยคถูกไวยากรณ์จากคำที่กำหนด และตอบอีเมลครบประเด็น / Grammatical sentences & email replies.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"60 นาที",ac:"โครงประโยคจากภาพ (ใช้ 2 คำที่ให้) + โครงตอบอีเมล",acEn:"Sentence & email structure"},
     {tm:"55 นาที",ac:"เขียนจริง + ตรวจด้วย Grammarly",acEn:"Write & check"},
     {tm:"20 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนวิธีเขียนประโยคจากภาพโดยใช้ 2 คำที่กำหนดให้ครบ",
     "เรียนโครงตอบอีเมล: ทักทาย → ตอบครบทุกคำสั่ง → ปิดท้าย",
     "เขียนประโยคจากภาพ 5 ข้อ + ตอบอีเมล 1 ฉบับ",
     "ตรวจงานด้วย Grammarly แล้วแก้ที่ผิด"],
   game:{name:"Grammarly Challenge",desc:"เขียน 5 ประโยค ให้ Grammarly ตรวจ ตั้งเป้า 0 error",url:"grammarly.com"},
   tip:"อีเมล TOEIC ต้องตอบ 'ทุกคำสั่ง' ในโจทย์ — นับให้ครบก่อนส่ง มักมี 2-3 คำสั่งซ่อนอยู่"},
  {id:"d20", day:20, th:"🎯 สอบซ้อมครั้งที่ 1 (L&R เต็ม)", en:"🎯 MOCK TEST 1 (Full L&R)", skills:["M"], time:"4 ชม.",
   goal:"จำลองสนามจริง วัดคะแนนกลางคอร์ส / Simulate the real test, measure mid-course score.",
   schedule:[
     {tm:"10 นาที",ac:"เตรียมพร้อมเหมือนสอบจริง",acEn:"Set up like the real exam"},
     {tm:"120 นาที",ac:"สอบ Listening 45' + Reading 75' ต่อเนื่อง",acEn:"Full L&R, no breaks"},
     {tm:"60 นาที",ac:"ตรวจคะแนน + วิเคราะห์ทุกข้อที่ผิด",acEn:"Score & full error analysis"},
     {tm:"30 นาที",ac:"อัปเดตแผน: เจาะจุดอ่อนที่เหลือ",acEn:"Update plan for weak areas"}],
   tasks:["ทำ Mock Test 1 (Listening + Reading) จับเวลาต่อเนื่องไม่พัก",
     "ตรวจคะแนนแปลงเป็นสเกล TOEIC (โดยประมาณ)",
     "เทียบกับ diagnostic — พัฒนากี่คะแนน?",
     "วิเคราะห์ทุกข้อที่ผิด แยกเป็น 'ไม่รู้' vs 'พลาด'",
     "เขียนแผนสัปดาห์ 5–8 เจาะ 3 จุดอ่อนใหญ่สุด"],
   game:{name:"พักสมอง!",desc:"วันนี้สอบหนัก — จบแล้วพักผ่อน ให้รางวัลตัวเอง ไม่ต้องเล่นเกมฝึกก็ได้",url:""},
   tip:"Mock test ไม่ใช่แค่วัดคะแนน แต่คือ 'ซ้อมความอึด' 2 ชั่วโมงเต็ม — ร่างกายต้องชินด้วย"}
]},
{n:5, color:"var(--green)", th:"อุดจุดอ่อน + สร้างการพูด", en:"Fix Gaps + Build Speaking", days:[
  {id:"d21", day:21, th:"วิเคราะห์ Mock 1 + อุดจุดอ่อน", en:"Analyze Mock 1 + Patch Weaknesses", skills:["G","R","RV"], time:"3 ชม.",
   goal:"เปลี่ยนข้อผิดใน mock เป็นบทเรียน / Turn mistakes into targeted lessons.",
   schedule:[
     {tm:"15 นาที",ac:"เปิด error-log จาก mock",acEn:"Open mock error-log"},
     {tm:"80 นาที",ac:"เรียนซ้ำหัวข้อที่ผิดเยอะสุด 2–3 เรื่อง",acEn:"Re-learn top weak topics"},
     {tm:"60 นาที",ac:"ฝึกโจทย์เฉพาะจุดอ่อน 30 ข้อ",acEn:"Targeted 30-item drill"},
     {tm:"25 นาที",ac:"เกม + จดสรุป",acEn:"Game + notes"}],
   tasks:["จัดอันดับจุดอ่อนจาก Mock 1 (พาร์ท/หัวข้อ)",
     "เรียนซ้ำ 2–3 หัวข้อที่ผิดเยอะสุด",
     "ฝึกโจทย์เจาะจุดอ่อน 30 ข้อ",
     "อัปเดต flashcard คำ/โครงสร้างที่ยังพลาด"],
   game:{name:"Kahoot/Quizizz จุดอ่อน",desc:"ค้นควิซหัวข้อที่ตัวเองอ่อน เล่นซ้ำจนแม่น",url:"kahoot.com"},
   tip:"'ข้อที่พลาดเพราะเลินเล่อ' แก้ง่ายกว่า 'ข้อที่ไม่รู้' — จัดการเลินเล่อก่อน ได้คะแนนเร็ว"},
  {id:"d22", day:22, th:"ฝึกความเร็วการฟัง + Dictation", en:"Listening Speed + Dictation", skills:["L"], time:"3 ชม.",
   goal:"ฟังทันความเร็วเจ้าของภาษา และจับทุกคำด้วย dictation / Keep up with native speed.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มหูที่ 1.2x",acEn:"Warm up at 1.2x speed"},
     {tm:"75 นาที",ac:"Dictation Part 3/4 (ฟัง–เขียนทุกคำ)",acEn:"Dictation practice"},
     {tm:"60 นาที",ac:"ฝึก Part 3&4 ที่ความเร็ว 1.1–1.2x",acEn:"Practice at 1.1-1.2x"},
     {tm:"30 นาที",ac:"Shadowing + เกม",acEn:"Shadowing + game"}],
   tasks:["ทำ dictation 1 บทสนทนา (ฟังแล้วเขียนทุกคำ เทียบ transcript)",
     "ฝึกฟัง Part 3&4 เร่งความเร็ว 1.1–1.2x",
     "Shadowing บทที่เร็วที่สุดจนพูดทัน",
     "จดคำที่ฟังไม่ทันบ่อยๆ (เสียงเชื่อม/เสียงหาย)"],
   game:{name:"Shadowing Challenge (YouTube)",desc:"เลือกคลิป 1 นาที พูดตามให้ทันทุกคำ อัดเทียบต้นฉบับ",url:"youtube.com"},
   tip:"ถ้าฟัง 1.2x ได้ พอเจอความเร็วจริงในสนามสอบจะรู้สึก 'ช้าลง' ทันที — เทคนิคเก่าแต่ได้ผล"},
  {id:"d23", day:23, th:"Speaking: ตอบคำถาม + ใช้ข้อมูลตอบ", en:"Speaking: Respond to Questions + Using Info", skills:["S"], time:"2.5 ชม.",
   goal:"ตอบคำถามภายในเวลา และดึงข้อมูลจากตารางมาตอบ / Answer on time using given info.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มปาก",acEn:"Warm-up"},
     {tm:"60 นาที",ac:"เทคนิคตอบคำถาม 3 ข้อ + respond using information",acEn:"Technique"},
     {tm:"55 นาที",ac:"อัดเสียงทำโจทย์ครบชุด + ฟังซ้ำ",acEn:"Record full set"},
     {tm:"20 นาที",ac:"เกมออกเสียง",acEn:"Pronunciation game"}],
   tasks:["เรียนเทคนิคตอบคำถามสั้น-ยาว ภายในเวลาที่กำหนด",
     "เรียน respond using information (อ่านตาราง 45 วิ แล้วตอบ)",
     "อัดเสียงทำโจทย์ทั้ง 2 แบบ อย่างละ 2 ข้อ",
     "ฟังซ้ำ จับ 'คำเชื่อม' และความคล่อง (fluency)"],
   game:{name:"ELSA + อัดเสียงเอง",desc:"ฝึกออกเสียงใน ELSA แล้วอัดตอบโจทย์จริง เทียบความคล่องแต่ละวัน",url:"elsaspeak.com"},
   tip:"ตอบไม่ต้องเป๊ะเหมือนเรียงความ ขอแค่ 'พูดต่อเนื่อง ไม่เงียบนาน' คะแนน fluency สำคัญมาก"},
  {id:"d24", day:24, th:"การอ่าน: Skim/Scan + บริหารเวลา", en:"Reading: Skim/Scan + Time Management", skills:["R"], time:"3 ชม.",
   goal:"อ่าน Part 7 ให้ทันเวลา ด้วยการกวาดตาแบบมีระบบ / Finish Part 7 on time.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์ม",acEn:"Warm-up"},
     {tm:"70 นาที",ac:"เทคนิค skim (ใจความ) & scan (หาข้อมูลเฉพาะ) + แผนเวลา",acEn:"Skim/scan + time plan"},
     {tm:"70 นาที",ac:"ฝึก Part 7 mix จับเวลาเข้ม",acEn:"Timed Part 7 mix"},
     {tm:"25 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["วางแผนเวลา Reading 75 นาที: Part 5 (10') Part 6 (8') Part 7 (57')",
     "ฝึก skim หา main idea ใน 20 วินาที/บทความ",
     "ฝึก Part 7 แบบผสม จับเวลาตามแผน",
     "ถ้าติดข้อไหนเกิน 1 นาที ให้เดา+มาร์ก แล้วไปต่อ"],
   game:{name:"Timed Reading Race",desc:"ตั้งเวลา แข่งกับตัวเอง อ่านบทความ+ตอบให้ทันทุกครั้งที่ดีขึ้น",url:"newsinlevels.com"},
   tip:"คนสอบไม่ทันเพราะ 'ดันทุรังกับข้อยาก' — ฝึกวินัย 'ปล่อยข้อยาก' คือหัวใจของการทำทัน"},
  {id:"d25", day:25, th:"รีวิวสัปดาห์ 5", en:"Week 5 Review", skills:["RV"], time:"2 ชม.",
   goal:"รวบยอดฟัง+อ่าน+พูดของสัปดาห์ / Consolidate L, R & S.",
   schedule:[
     {tm:"40 นาที",ac:"mini-test ผสม L+R 30 ข้อ",acEn:"Mixed 30-item test"},
     {tm:"35 นาที",ac:"ทบทวน speaking ที่อัดไว้",acEn:"Review recorded speaking"},
     {tm:"25 นาที",ac:"วันเล่นเกม!",acEn:"Game day!"},
     {tm:"20 นาที",ac:"ทบทวน flashcard",acEn:"Flashcard review"}],
   tasks:["ทำ mini-test ผสม Listening+Reading 30 ข้อ",
     "ฟัง speaking ที่อัดสัปดาห์นี้ เทียบพัฒนาการ",
     "ทบทวน flashcard สะสม (100+ คำ)",
     "อัปเดต error-log"],
   game:{name:"เลือกเกมโปรด",desc:"เล่นเกมที่ชอบที่สุด 25 นาที เป็นรางวัลจบสัปดาห์",url:""},
   tip:"ครึ่งทางแล้ว! กลับไปดูคะแนน diagnostic วันแรก — คุณมาไกลกว่าที่คิดแน่นอน"}
]},
{n:6, color:"var(--pink)", th:"ขั้นสูง + สร้างการเขียน", en:"Advanced + Build Writing", days:[
  {id:"d26", day:26, th:"Part 7 ขั้นสูง: อนุมาน & ข้ามบทความ", en:"Part 7 Advanced: Inference & Cross-text", skills:["R"], time:"3 ชม.",
   goal:"ตอบคำถามอนุมานและ 'ประโยคแทรก' ในบทความยาว / Inference & sentence-placement.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์ม",acEn:"Warm-up"},
     {tm:"75 นาที",ac:"คำถาม inference, purpose, sentence-insertion",acEn:"Advanced question types"},
     {tm:"70 นาที",ac:"ฝึกบทความยากจับเวลา",acEn:"Timed hard passages"},
     {tm:"20 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนคำถาม inference & purpose ('Why was this written?')",
     "เรียน sentence-insertion (วางประโยคในตำแหน่งที่ถูก)",
     "ฝึกบทความยาก/ยาว จับเวลา 4 ชุด",
     "จดสำนวนที่บ่งบอกนัยในบทอ่าน"],
   game:{name:"อ่านบทความจริง (Medium/BBC)",desc:"อ่านบทความจริง 1 ชิ้น เดา 'จุดประสงค์ผู้เขียน' ฝึก inference",url:"bbc.com/news"},
   tip:"คำถาม inference คำตอบ 'ไม่ได้เขียนตรงๆ' ในบทความ แต่ต้อง 'สรุปได้จากที่เขียน' — ระวังตัวเลือกที่ตรงเกินไป"},
  {id:"d27", day:27, th:"Writing: เรียงความแสดงความเห็น", en:"Writing: Opinion Essay", skills:["W"], time:"3 ชม.",
   goal:"เขียน opinion essay มีโครงชัด 300 คำใน 30 นาที / Structured 300-word essay.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"70 นาที",ac:"โครงเรียงความ: intro–2 body–conclusion + คำเชื่อม",acEn:"Essay structure + connectors"},
     {tm:"70 นาที",ac:"เขียน 1 เรียงความจับเวลา + ตรวจ",acEn:"Write 1 timed essay & check"},
     {tm:"25 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนโครง opinion essay: intro (thesis) → 2 body + เหตุผล/ตัวอย่าง → conclusion",
     "เรียนคำเชื่อม: firstly, moreover, on the other hand, in conclusion",
     "เขียนเรียงความ 1 เรื่อง จับเวลา 30 นาที (~300 คำ)",
     "ตรวจด้วย Grammarly + นับคำเชื่อมที่ใช้"],
   game:{name:"Grammarly Essay Check",desc:"ให้ Grammarly ตรวจเรียงความ ตั้งเป้าลด error ทุกครั้ง",url:"grammarly.com"},
   tip:"กรรมการให้คะแนน 'โครงสร้าง+เหตุผล' มากกว่าความสวยของภาษา — ขอแค่ชัดเจนและมีตัวอย่าง"},
  {id:"d28", day:28, th:"Speaking: เสนอทางแก้ + แสดงความเห็น", en:"Speaking: Propose Solution + Express Opinion", skills:["S"], time:"2.5 ชม.",
   goal:"พูดตอบปัญหาและแสดงความเห็นได้อย่างมีเหตุผลภายในเวลา / Solve & opine fluently.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มปาก",acEn:"Warm-up"},
     {tm:"60 นาที",ac:"โครง propose solution + express opinion (60 วิ)",acEn:"Response structures"},
     {tm:"55 นาที",ac:"อัดเสียงทำโจทย์ + ฟังซ้ำ",acEn:"Record & review"},
     {tm:"20 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["เรียนโครง propose solution: รับปัญหา → เสนอวิธี → เหตุผล",
     "เรียนโครง express opinion: จุดยืน → 2 เหตุผล → สรุป",
     "อัดเสียงทำอย่างละ 2 ข้อ ภายในเวลาจริง",
     "ฟังซ้ำ จับความต่อเนื่องและคำเชื่อม"],
   game:{name:"HelloTalk / อภิปรายกับเพื่อน",desc:"คุยหัวข้อความเห็นกับเจ้าของภาษาหรือเพื่อน ฝึกพูดสด",url:"hellotalk.com"},
   tip:"ไม่มี 'ความเห็นถูก/ผิด' — กรรมการฟัง 'เหตุผลชัดไหม พูดคล่องไหม' เลือกจุดยืนที่พูดง่ายที่สุด"},
  {id:"d29", day:29, th:"สำนวน คำผสม & คำเชื่อมย่อหน้า", en:"Idioms, Collocations & Connectors", skills:["V","R"], time:"2.5 ชม.",
   goal:"รู้คำที่มักไปด้วยกัน และคำเชื่อมใน Part 6 / Collocations & discourse markers.",
   schedule:[
     {tm:"15 นาที",ac:"ทบทวน",acEn:"Review"},
     {tm:"65 นาที",ac:"collocations (make/do/take) + phrasal verbs + connectors",acEn:"Collocations + connectors"},
     {tm:"45 นาที",ac:"ฝึก Part 6 เน้นคำเชื่อม 3 ชุด",acEn:"Part 6 connector drill"},
     {tm:"25 นาที",ac:"เกมศัพท์",acEn:"Vocab game"}],
   tasks:["เรียน collocations: make a decision, take responsibility, do research",
     "เรียน phrasal verbs ที่ออกบ่อย 15 ตัว",
     "เรียนคำเชื่อมย่อหน้า: however, therefore, in addition, nevertheless",
     "ฝึก Part 6 เน้นข้อคำเชื่อม 3 ชุด"],
   game:{name:"Quizlet (Collocations)",desc:"เล่นชุดคำผสม/phrasal verb แบบ Match และ Test",url:"quizlet.com"},
   tip:"TOEIC รักคำผสม — จำ 'make a decision' (ไม่ใช่ do a decision) เป็นก้อน ได้ทั้งฟังและอ่าน"},
  {id:"d30", day:30, th:"รีวิวสัปดาห์ 6", en:"Week 6 Review", skills:["RV"], time:"2 ชม.",
   goal:"รวบยอดอ่านขั้นสูง+เขียน+พูด / Consolidate advanced R, W & S.",
   schedule:[
     {tm:"40 นาที",ac:"ฝึก Part 7 ยาก 3 ชุด",acEn:"3 hard Part 7 sets"},
     {tm:"35 นาที",ac:"เขียน mini-essay 1 เรื่อง",acEn:"Write 1 mini-essay"},
     {tm:"25 นาที",ac:"วันเล่นเกม!",acEn:"Game day!"},
     {tm:"20 นาที",ac:"ทบทวน flashcard",acEn:"Flashcard review"}],
   tasks:["ฝึก Part 7 บทความยาก 3 ชุด",
     "เขียน mini-essay 1 เรื่อง จับเวลา 25 นาที",
     "อัด speaking express-opinion 1 ข้อ",
     "ทบทวน flashcard สะสม (120+ คำ)"],
   game:{name:"เลือกเกมโปรด",desc:"รางวัลจบสัปดาห์ — เล่นเกมที่ชอบ 25 นาที",url:""},
   tip:"เหลืออีก 2 สัปดาห์! ตอนนี้คุณครบเครื่องทั้ง 4 ทักษะแล้ว ที่เหลือคือ 'ขัดเงา' ให้คม"}
]},
{n:7, color:"var(--indigo)", th:"เก็งกลยุทธ์ + จับเวลา", en:"Strategy + Full-Section Timing", days:[
  {id:"d31", day:31, th:"ซ้อม Listening เต็มพาร์ท จับเวลา", en:"Full Listening Section (Timed)", skills:["L"], time:"2.5 ชม.",
   goal:"ทำ Listening 100 ข้อรวดเดียว สร้างความอึด / Full 100-item listening stamina.",
   schedule:[
     {tm:"10 นาที",ac:"วอร์มหู",acEn:"Warm-up"},
     {tm:"50 นาที",ac:"Listening เต็ม 100 ข้อ (Part 1–4)",acEn:"Full 100-item listening"},
     {tm:"50 นาที",ac:"ตรวจ + ฟังซ้ำข้อผิด + อ่าน transcript",acEn:"Review with transcript"},
     {tm:"20 นาที",ac:"Shadowing ข้อที่ยากสุด",acEn:"Shadow hardest items"}],
   tasks:["ทำ Listening เต็มพาร์ท 100 ข้อ จับเวลาจริง ~45 นาที",
     "ตรวจคะแนน เทียบ Mock 1",
     "ฟังซ้ำทุกข้อผิดพร้อม transcript",
     "จดประเภทกับดักที่ยังพลาด"],
   game:{name:"Shadowing มาราธอน",desc:"เลือก 3 ข้อที่ยากสุด shadow จนพูดทันเป๊ะ",url:"youtube.com"},
   tip:"หูล้าเป็นเรื่องจริงในนาทีที่ 30+ — การซ้อมเต็มพาร์ทคือการฝึก 'สมาธิยาว' ไม่ใช่แค่ทักษะฟัง"},
  {id:"d32", day:32, th:"ซ้อม Reading เต็มพาร์ท จับเวลา", en:"Full Reading Section (Timed)", skills:["R"], time:"3 ชม.",
   goal:"ทำ Reading 100 ข้อใน 75 นาทีให้ทัน / Finish 100 reading items in 75 min.",
   schedule:[
     {tm:"10 นาที",ac:"เตรียมแผนเวลา",acEn:"Set time plan"},
     {tm:"75 นาที",ac:"Reading เต็ม 100 ข้อ (Part 5–7)",acEn:"Full 100-item reading"},
     {tm:"60 นาที",ac:"ตรวจ + วิเคราะห์ข้อผิด + จับจุดกินเวลา",acEn:"Review + timing analysis"},
     {tm:"20 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["ทำ Reading เต็มพาร์ท 100 ข้อ ภายใน 75 นาที",
     "เช็ก: ทำทันไหม? ค้างกี่ข้อ?",
     "วิเคราะห์ข้อผิด + พาร์ทที่กินเวลามากสุด",
     "ปรับแผนเวลาสำหรับ Mock 2"],
   game:{name:"Timed Reading Race",desc:"อ่านบทความสั้นแข่งเวลา คลายเครียดหลังซ้อมหนัก",url:"newsinlevels.com"},
   tip:"ถ้าทำ Reading ไม่ทัน ปัญหามักอยู่ที่ Part 5/6 ช้า ไม่ใช่ Part 7 — จับเวลาต้นพาร์ทให้ดี"},
  {id:"d33", day:33, th:"ซ้อม Speaking เต็มชุด (11 ข้อ)", en:"Full Speaking Set (11 Questions)", skills:["S"], time:"2.5 ชม.",
   goal:"ทำ Speaking ครบ 11 ข้อแบบจับเวลา + อัดเสียงประเมิน / Full timed speaking test.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์มปาก",acEn:"Warm-up"},
     {tm:"40 นาที",ac:"ทำ Speaking ครบ 11 ข้อ อัดเสียง",acEn:"Full 11-item recorded"},
     {tm:"55 นาที",ac:"ฟังซ้ำ ประเมินตามเกณฑ์ (fluency/pronunciation/grammar)",acEn:"Self-score by rubric"},
     {tm:"20 นาที",ac:"ฝึกซ้ำข้อที่อ่อนสุด + ELSA",acEn:"Redo weakest + ELSA"}],
   tasks:["ทำ Speaking ครบทั้ง 11 ข้อ จับเวลาจริง อัดเสียง",
     "ประเมินตัวเองตามเกณฑ์: ออกเสียง/ความคล่อง/ไวยากรณ์/เนื้อหา",
     "ฝึกซ้ำ 2 ข้อที่คะแนนต่ำสุด",
     "จดคำ/เสียงที่ต้องปรับ"],
   game:{name:"ELSA Speak (โหมดจับเวลา)",desc:"ฝึกออกเสียงประโยคยาว ให้แอปให้คะแนน ปรับจนคะแนนสูง",url:"elsaspeak.com"},
   tip:"อัดเสียงตัวเองแล้วฟัง = วิธีพัฒนาการพูดที่เร็วที่สุด แม้จะเขินตอนแรก แต่เห็นผลชัดมาก"},
  {id:"d34", day:34, th:"ซ้อม Writing เต็มชุด (8 ข้อ)", en:"Full Writing Set (8 Questions)", skills:["W"], time:"2.5 ชม.",
   goal:"ทำ Writing ครบ 8 ข้อจับเวลา + ตรวจตามเกณฑ์ / Full timed writing test.",
   schedule:[
     {tm:"10 นาที",ac:"ทบทวนโครง",acEn:"Review structures"},
     {tm:"60 นาที",ac:"ทำ Writing ครบ 8 ข้อ จับเวลา",acEn:"Full 8-item writing"},
     {tm:"55 นาที",ac:"ตรวจด้วย Grammarly + เกณฑ์ + แก้",acEn:"Check & revise"},
     {tm:"20 นาที",ac:"เกม",acEn:"Game"}],
   tasks:["ทำ Writing ครบ 8 ข้อ (5 ประโยคจากภาพ + 2 อีเมล + 1 เรียงความ) จับเวลา ~60 นาที",
     "ตรวจด้วย Grammarly แล้วแก้ทุกจุด",
     "เช็กเรียงความ: มีครบ intro-body-conclusion ไหม?",
     "จดข้อผิดไวยากรณ์ที่ซ้ำบ่อย"],
   game:{name:"Grammarly Streak",desc:"เขียนย่อหน้าสั้นทุกวัน ให้ Grammarly ตรวจ สะสมสถิติ error ลดลง",url:"grammarly.com"},
   tip:"บริหารเวลา Writing: ประโยคจากภาพเร็วๆ เก็บเวลาไปทุ่มเรียงความ (ข้อคะแนนเยอะสุด)"},
  {id:"d35", day:35, th:"รีวิวสัปดาห์ 7 + เจาะจุดอ่อนสุดท้าย", en:"Week 7 Review + Final Weak Spots", skills:["RV"], time:"2 ชม.",
   goal:"ปิดจุดอ่อนที่เหลือก่อนสอบซ้อมรอบสุดท้าย / Close remaining gaps before Mock 2.",
   schedule:[
     {tm:"45 นาที",ac:"เจาะโจทย์จุดอ่อนที่เหลือ 30 ข้อ",acEn:"Targeted 30-item drill"},
     {tm:"35 นาที",ac:"ทบทวน flashcard + error-log ทั้งหมด",acEn:"Review all notes"},
     {tm:"25 นาที",ac:"วันเล่นเกม!",acEn:"Game day!"},
     {tm:"15 นาที",ac:"วางแผน Mock 2",acEn:"Plan Mock 2"}],
   tasks:["ฝึกโจทย์เจาะ 3 จุดอ่อนที่เหลือ 30 ข้อ",
     "อ่าน error-log ทั้งหมดตั้งแต่ต้นคอร์ส",
     "ทบทวน flashcard สะสม (140+ คำ)",
     "เตรียมพร้อมร่างกาย+เวลา สำหรับ Mock 2 พรุ่งนี้"],
   game:{name:"เลือกเกมโปรด",desc:"ผ่อนคลายก่อนสอบซ้อมใหญ่ — เล่นเกมที่ชอบ 25 นาที",url:""},
   tip:"คืนก่อน Mock 2 อย่าอ่านหนัก — สมองที่พักพอจะทำข้อสอบได้ดีกว่าสมองที่ล้า"}
]},
{n:8, color:"var(--gold)", th:"ขัดเงาขั้นสุดท้าย + สอบซ้อม 2", en:"Final Polish + Mock Test 2", days:[
  {id:"d36", day:36, th:"🏁 สอบซ้อมครั้งที่ 2 (L&R เต็ม)", en:"🏁 MOCK TEST 2 (Full L&R)", skills:["M"], time:"4 ชม.",
   goal:"วัดคะแนนสุดท้าย เทียบเป้า / Final score check against your target.",
   schedule:[
     {tm:"10 นาที",ac:"เตรียมพร้อมเหมือนสอบจริง",acEn:"Set up like real exam"},
     {tm:"120 นาที",ac:"สอบ Listening 45' + Reading 75' ต่อเนื่อง",acEn:"Full L&R, no breaks"},
     {tm:"60 นาที",ac:"ตรวจคะแนน + วิเคราะห์ทุกข้อผิด",acEn:"Score & full analysis"},
     {tm:"30 นาที",ac:"เทียบ Mock 1 + เป้าหมาย",acEn:"Compare to Mock 1 & goal"}],
   tasks:["ทำ Mock Test 2 (L+R) จับเวลาต่อเนื่องไม่พัก",
     "ตรวจคะแนนแปลงเป็นสเกล TOEIC",
     "เทียบ Mock 1 vs Mock 2 vs diagnostic — เส้นทางพัฒนาการ",
     "ถึงเป้าหมายหรือยัง? เหลือจุดไหนต้องเก็บ 4 วันสุดท้าย"],
   game:{name:"พักสมอง!",desc:"สอบหนักวันนี้ — พักผ่อนเต็มที่ ให้รางวัลตัวเอง",url:""},
   tip:"ไม่ว่าคะแนนออกมาเท่าไร ให้ภูมิใจ — คุณซ้อมมา 36 วันแล้ว นั่นคือวินัยที่คนส่วนใหญ่ทำไม่ได้"},
  {id:"d37", day:37, th:"วิเคราะห์ Mock 2 + ซ้อม S&W", en:"Analyze Mock 2 + S&W Mock", skills:["S","W","RV"], time:"3 ชม.",
   goal:"อุดจุดอ่อนสุดท้ายจาก Mock 2 และซ้อม S&W เต็มรูปแบบ / Patch final gaps + S&W mock.",
   schedule:[
     {tm:"15 นาที",ac:"เปิด error-log Mock 2",acEn:"Open Mock 2 log"},
     {tm:"70 นาที",ac:"เรียนซ้ำจุดอ่อนที่เหลือ + ฝึกโจทย์",acEn:"Re-learn + drill"},
     {tm:"70 นาที",ac:"ซ้อม Speaking + Writing เต็มชุด อัด/ตรวจ",acEn:"Full S&W mock"},
     {tm:"25 นาที",ac:"เกม + สรุป",acEn:"Game + wrap"}],
   tasks:["จัดอันดับจุดอ่อนสุดท้ายจาก Mock 2",
     "ฝึกโจทย์เจาะจุดอ่อน 25 ข้อ",
     "ซ้อม Speaking 11 ข้อ + Writing 8 ข้อ อีกรอบ",
     "ตรวจ S&W ตามเกณฑ์ จดสิ่งที่ต้องปรับ"],
   game:{name:"Kahoot จุดอ่อน + ELSA",desc:"เล่นควิซหัวข้ออ่อน แล้วขัดออกเสียงด้วย ELSA",url:"kahoot.com"},
   tip:"4 วันสุดท้ายเน้น 'ของที่เกือบได้' — คะแนนขึ้นเร็วสุดจากการเก็บข้อที่พลาดเพราะเลินเล่อ"},
  {id:"d38", day:38, th:"เก็บศัพท์รอบสุดท้าย + กับดักยอดฮิต", en:"Final Vocab Blitz + Common Traps", skills:["V","G"], time:"2.5 ชม.",
   goal:"รีเฟรชศัพท์สะสมและทบทวนกับดักที่เจอบ่อยสุด / Refresh vocab & top traps.",
   schedule:[
     {tm:"15 นาที",ac:"วอร์ม",acEn:"Warm-up"},
     {tm:"60 นาที",ac:"ทบทวน flashcard สะสมทั้งหมด (150+ คำ)",acEn:"Review all flashcards"},
     {tm:"45 นาที",ac:"ทบทวนกับดักทุกพาร์ทจาก error-log",acEn:"Review all traps"},
     {tm:"25 นาที",ac:"เกมศัพท์รวม",acEn:"Vocab game"}],
   tasks:["ทบทวน flashcard สะสมทั้งหมด เร่งความเร็วการจำ",
     "อ่านสรุปกับดักยอดฮิตทุกพาร์ท (Part 1 คำพ้องเสียง, Part 5 word form ฯลฯ)",
     "ทำ mini-quiz ศัพท์ 30 ข้อ",
     "จดคำ 'ที่ยังไม่แน่ใจ' ไว้ทบทวนวันสุดท้าย"],
   game:{name:"Quizlet Test (โหมดสุ่ม)",desc:"ทดสอบศัพท์สะสมแบบสุ่ม เก็บคะแนนให้สูงสุด",url:"quizlet.com"},
   tip:"อย่าเรียนศัพท์ 'ใหม่' ช่วงนี้ — ตอกย้ำ 'ของเดิม' ให้แน่น คุ้มกว่าและไม่สับสน"},
  {id:"d39", day:39, th:"รีวิวเบาๆ + สรุปกลยุทธ์ + พักใจ", en:"Light Review + Strategy Recap + Rest", skills:["RV"], time:"2 ชม.",
   goal:"ทบทวนแบบเบา เก็บความมั่นใจ ไม่โหมหนัก / Light review, build confidence.",
   schedule:[
     {tm:"40 นาที",ac:"อ่านสรุปกลยุทธ์แต่ละพาร์ท",acEn:"Read part-by-part strategy"},
     {tm:"35 นาที",ac:"ทำโจทย์เบาๆ พาร์ทที่ถนัด (เรียกความมั่นใจ)",acEn:"Easy confidence drill"},
     {tm:"25 นาที",ac:"ทบทวนแผนเวลาในห้องสอบ",acEn:"Rehearse time plan"},
     {tm:"20 นาที",ac:"พักผ่อน + เตรียมของสำหรับพรุ่งนี้",acEn:"Rest + pack"}],
   tasks:["อ่านสรุปกลยุทธ์ทีละพาร์ท (ทำอะไรก่อน-หลัง)",
     "ทำโจทย์พาร์ทที่ถนัด 15 ข้อ เพื่อเรียกความมั่นใจ",
     "ซ้อมแผนบริหารเวลาในหัวอีกครั้ง",
     "เตรียมของสอบตาม 'เช็กลิสต์วันสอบจริง' ด้านล่าง"],
   game:{name:"ดูคลิปให้กำลังใจ + Duolingo เบาๆ",desc:"ดูคลิปเทคนิคสั้นๆ ให้กำลังใจ แล้วเล่น Duolingo คงสตรีคแบบสบายๆ",url:"duolingo.com"},
   tip:"วันนี้ 'อย่าโหม' — เป้าหมายคือเข้าห้องสอบด้วยสมองสดและมั่นใจ ไม่ใช่สมองล้า"},
  {id:"d40", day:40, th:"🎓 จำลองสนามจริง + พร้อมสอบ", en:"🎓 Exam Simulation + Ready to Go", skills:["M","RV"], time:"2.5 ชม.",
   goal:"จำลองบรรยากาศสอบครั้งสุดท้าย เข้าห้องสอบอย่างมั่นใจ / Final sim, walk in confident.",
   schedule:[
     {tm:"10 นาที",ac:"วอร์มหู 10 นาที (เหมือนเช้าวันสอบ)",acEn:"Ear warm-up like exam morning"},
     {tm:"60 นาที",ac:"จำลองครึ่งชุด L+R ตามเวลาจริง (เบาๆ)",acEn:"Half-set simulation"},
     {tm:"40 นาที",ac:"ทบทวนกลยุทธ์+กับดักครั้งสุดท้าย",acEn:"Final strategy review"},
     {tm:"20 นาที",ac:"เช็กลิสต์วันสอบ + ให้กำลังใจตัวเอง",acEn:"Exam checklist + self pep-talk"}],
   tasks:["จำลองครึ่งชุด L+R ตามเวลาจริง (ไม่ต้องเต็ม เพื่อไม่ให้ล้า)",
     "อ่านสรุปกลยุทธ์+กับดักครั้งสุดท้าย",
     "ทำตาม 'เช็กลิสต์วันสอบจริง' ให้ครบ",
     "เขียนให้กำลังใจตัวเอง 1 ประโยค — คุณพร้อมแล้ว!"],
   game:{name:"ฉลองความสำเร็จ! 🎉",desc:"จบคอร์ส 40 วันแล้ว! ให้รางวัลตัวเองเต็มที่ พรุ่งนี้ไปลุยสนามจริง",url:""},
   tip:"คุณเดินทางครบ 60 วันแล้ว — ความมั่นใจของคุณมาจากการซ้อมจริง ไม่ใช่โชค เข้าไปคว้าคะแนนเป้าเลย!"}
]}
];

/* ============================================================
   ACHIEVEMENTS
   ============================================================ */
const ACHIEVEMENTS = [
  {id:"start",  em:"🎯", th:"ออกสตาร์ท",       en:"First Step",     test:s=>dayDone("d1",s)},
  {id:"wk1",    em:"📅", th:"จบสัปดาห์แรก",     en:"Week 1 Clear",   test:s=>weekDone(0,s)},
  {id:"half",   em:"🔥", th:"ครึ่งทางแล้ว",     en:"Halfway Hero",   test:s=>pctDone(s)>=50},
  {id:"mock1",  em:"📝", th:"ผ่านสอบซ้อม 1",    en:"Mock 1 Done",    test:s=>dayDone("d20",s)},
  {id:"speak",  em:"🗣️", th:"นักพูดตัวจริง",    en:"Speaker Unlocked",test:s=>dayDone("d33",s)},
  {id:"write",  em:"✏️", th:"นักเขียนตัวจริง",   en:"Writer Unlocked",test:s=>dayDone("d34",s)},
  {id:"mock2",  em:"🏁", th:"ผ่านสอบซ้อม 2",    en:"Mock 2 Done",    test:s=>dayDone("d36",s)},
  {id:"finish", em:"🏆", th:"จบหลักสูตร!",      en:"Course Complete",test:s=>pctDone(s)>=100}
];

/* ============================================================
   STATE + LOGIC
   ============================================================ */
const KEY="toeic60_progress_v1";
let state=load();

function load(){
  try{const s=JSON.parse(localStorage.getItem(KEY));if(s&&s.checked)return s;}catch(e){}
  return {checked:{},streak:0,lastActive:null};
}
function save(){localStorage.setItem(KEY,JSON.stringify(state));}

const allDays=WEEKS.flatMap(w=>w.days);
const totalTasks=allDays.reduce((n,d)=>n+d.tasks.length,0);

function taskId(d,i){return d.id+"-t"+i;}
function dayDone(id,s){const d=allDays.find(x=>x.id===id);if(!d)return false;
  return d.tasks.every((_,i)=>s.checked[taskId(d,i)]);}
function weekDone(wi,s){return WEEKS[wi].days.every(d=>d.tasks.every((_,i)=>s.checked[taskId(d,i)]));}
function tasksDone(s){return Object.values(s.checked).filter(Boolean).length;}
function daysDone(s){return allDays.filter(d=>dayDone(d.id,s)).length;}
function pctDone(s){return Math.round(tasksDone(s)/totalTasks*100);}
function xp(s){return tasksDone(s)*10 + daysDone(s)*40;}
function rankOf(x){let r=RANKS[0],idx=0;RANKS.forEach((rk,i)=>{if(x>=rk.min){r=rk;idx=i;}});return {r,idx};}

/* streak: update on any check activity */
function touchStreak(){
  const today=new Date().toISOString().slice(0,10);
  if(state.lastActive===today)return;
  const y=new Date(Date.now()-864e5).toISOString().slice(0,10);
  state.streak=(state.lastActive===y)?(state.streak+1):1;
  state.lastActive=today;
}

/* ============================================================
   RENDER
   ============================================================ */
const skillMap={L:"🎧 Listening",R:"📖 Reading",G:"⚔️ Grammar",V:"🔤 Vocab",
  S:"🗣️ Speaking",W:"✏️ Writing",RV:"🔁 Review",M:"🎯 Mock/Test"};

function renderWeeks(){
  const host=document.getElementById("weeks");host.innerHTML="";
  WEEKS.forEach((w,wi)=>{
    const wk=document.createElement("div");wk.className="week"+(wi===0?" open":"");
    wk.style.setProperty("--wk",w.color);
    const done=w.days.filter(d=>dayDone(d.id,state)).length;
    wk.innerHTML=`
      <div class="week-head" data-wk="${wi}">
        <div class="wk-no">${w.n}</div>
        <div class="wk-meta">
          <h3>สัปดาห์ ${w.n}: ${w.th}</h3>
          <small>Week ${w.n} · ${w.en}</small>
        </div>
        <div class="wk-prog"><b class="wkpct">0%</b><br><span class="wkdone">${done}/${w.days.length} วัน</span></div>
        <div class="chev">▼</div>
      </div>
      <div class="week-body">
        <div class="wk-bar"><i class="wkbar"></i></div>
        <div class="daylist"></div>
      </div>`;
    const list=wk.querySelector(".daylist");
    w.days.forEach(d=>list.appendChild(renderDay(d)));
    host.appendChild(wk);
    wk.querySelector(".week-head").addEventListener("click",()=>wk.classList.toggle("open"));
  });
}

function renderDay(d){
  const el=document.createElement("div");el.className="day";el.id="day-"+d.id;
  if(d.skills.includes("M"))el.classList.add("milestone");
  const tags=d.skills.map(s=>`<span class="tag ${s}">${skillMap[s]}</span>`).join("");
  const sched=d.schedule.map(b=>`<div class="block"><span class="tm">${b.tm}</span>
     <span class="ac">${b.ac}<small>${b.acEn}</small></span></div>`).join("");
  const tasks=d.tasks.map((t,i)=>{
    const id=taskId(d,i);const on=state.checked[id]?"checked":"";
    return `<div class="task"><input type="checkbox" id="${id}" ${on} data-day="${d.id}">
       <label for="${id}">${t}</label></div>`;}).join("");
  const gameUrl=d.game.url?` &nbsp;<a href="https://${d.game.url}" target="_blank" rel="noopener">🔗 ${d.game.url}</a>`:"";
  el.innerHTML=`
    <div class="day-head">
      <div class="day-no">${d.day}</div>
      <div class="day-title">
        <h4>Day ${d.day}: ${d.th}</h4>
        <div class="en">${d.en}</div>
        <div class="goal">🎯 <b>เป้าหมาย:</b> ${d.goal}</div>
        <div class="skill-tags">${tags}</div>
      </div>
      <div class="day-time">⏱️ <b>${d.time}</b></div>
    </div>
    <div class="day-body">
      <div class="schedule-title">🗓️ แพลนวันนี้ / Today's plan</div>
      ${sched}
      <div class="tasks-title">✅ ภารกิจ / Checklist (+10 XP ต่อข้อ)</div>
      ${tasks}
      <div class="game">
        <div class="g-name">🎮 เกมท้ายบท / After-class game: ${d.game.name}</div>
        <div class="g-desc">${d.game.desc}${gameUrl}</div>
      </div>
      <div class="tipbox">💡 <b>เคล็ดลับครู:</b> ${d.tip}</div>
    </div>`;
  el.querySelectorAll('input[type=checkbox]').forEach(cb=>{
    cb.addEventListener("change",onCheck);
  });
  return el;
}

function renderBadges(){
  const host=document.getElementById("badges");host.innerHTML="";
  ACHIEVEMENTS.forEach(a=>{
    const on=a.test(state);
    const b=document.createElement("div");b.className="bdg"+(on?" on":"");
    b.innerHTML=`<span class="em">${a.em}</span><span class="t">${a.th}<small>${a.en}</small></span>`;
    host.appendChild(b);
  });
}

function renderGamesMaster(){
  const host=document.getElementById("gamesMaster");host.innerHTML="";
  GAMES_MASTER.forEach(g=>{
    const c=document.createElement("div");c.className="gcard";
    c.innerHTML=`<h4>${g.em} ${g.name}</h4><div class="for">${g.for}</div>
      <p>${g.desc}</p>${g.tools.map(t=>`<div class="tool">• ${t}</div>`).join("")}`;
    host.appendChild(c);
  });
}

function updateDashboard(){
  const x=xp(state);const {r,idx}=rankOf(x);
  const next=RANKS[idx+1];
  document.getElementById("xpNow").textContent=x.toLocaleString();
  document.getElementById("rankEmoji").textContent=r.emoji;
  document.getElementById("rankName").childNodes[0].nodeValue=r.th;
  document.getElementById("rankNameEn").textContent=`${r.en} · Level ${idx+1}`;

  let pctRing,toGoTxt;
  if(next){
    const span=next.min-r.min;const into=x-r.min;
    pctRing=Math.min(100,Math.round(into/span*100));
    document.getElementById("xpNext").textContent=next.min.toLocaleString();
    toGoTxt=`อีก ${(next.min-x).toLocaleString()} XP เลื่อนเป็น ${next.th}`;
  }else{pctRing=100;document.getElementById("xpNext").textContent="MAX";toGoTxt="🏆 ถึงแรงก์สูงสุดแล้ว!";}
  document.getElementById("xpBar").style.width=pctRing+"%";
  document.getElementById("xpToGo").textContent=toGoTxt;
  document.getElementById("ring").style.setProperty("--deg",(pctRing*3.6)+"deg");

  document.getElementById("stPct").textContent=pctDone(state)+"%";
  document.getElementById("stDays").innerHTML=daysDone(state)+'<span style="font-size:14px;color:var(--muted)">/40</span>';
  document.getElementById("stStreak").textContent=state.streak+" 🔥";
  document.getElementById("stTasks").textContent=tasksDone(state);

  // per-week bars
  document.querySelectorAll(".week").forEach((wk,wi)=>{
    const w=WEEKS[wi];const done=w.days.filter(d=>dayDone(d.id,state)).length;
    const tt=w.days.reduce((n,d)=>n+d.tasks.length,0);
    const dt=w.days.reduce((n,d)=>n+d.tasks.filter((_,i)=>state.checked[taskId(d,i)]).length,0);
    const p=Math.round(dt/tt*100);
    wk.querySelector(".wkbar").style.width=p+"%";
    wk.querySelector(".wkpct").textContent=p+"%";
    wk.querySelector(".wkdone").textContent=`${done}/${w.days.length} วัน`;
  });

  // day done styling
  allDays.forEach(d=>{
    const el=document.getElementById("day-"+d.id);
    if(el)el.classList.toggle("done",dayDone(d.id,state));
  });
}

let prevBadges=new Set();
function checkNewBadges(){
  ACHIEVEMENTS.forEach(a=>{if(a.test(state)&&!prevBadges.has(a.id)){
    prevBadges.add(a.id);toast(`🏅 ปลดล็อกเหรียญ: ${a.th}!`);}});
}
function toast(msg){
  const t=document.getElementById("toast");t.textContent=msg;t.classList.add("show");
  clearTimeout(t._h);t._h=setTimeout(()=>t.classList.remove("show"),2600);
}

function onCheck(e){
  const id=e.target.id;
  state.checked[id]=e.target.checked;
  if(e.target.checked)touchStreak();
  save();
  updateDashboard();
  renderBadges();
  checkNewBadges();
}

/* rotating motivational quotes */
const QUOTES=[
 '"เก่งไม่ได้มาจากพรสวรรค์ แต่มาจากการซ้อมที่สนุกทุกวัน" — ครูของเธอ 💪',
 '"ทุกข้อที่ผิดวันนี้ คือคะแนนที่ได้เพิ่มในวันสอบ" 📈',
 '"ช้าๆ แต่ทุกวัน ชนะเร็วๆ แต่ทำวันเดียว" 🐢',
 '"อย่าเปรียบเทียบกับคนอื่น เปรียบเทียบกับตัวเองเมื่อวาน" ✨',
 '"ความมั่นใจในห้องสอบ มาจากเหงื่อในห้องซ้อม" 🔥'
];

/* init */
function init(){
  renderWeeks();renderGamesMaster();renderBadges();updateDashboard();
  ACHIEVEMENTS.forEach(a=>{if(a.test(state))prevBadges.add(a.id);});
  document.getElementById("quote").textContent=QUOTES[Math.floor(Math.random()*QUOTES.length)];
  document.getElementById("resetBtn").addEventListener("click",()=>{
    if(confirm("ล้างความคืบหน้าทั้งหมด? / Reset all progress? การกระทำนี้ย้อนกลับไม่ได้")){
      state={checked:{},streak:0,lastActive:null};prevBadges=new Set();save();
      renderWeeks();renderBadges();updateDashboard();toast("ล้างข้อมูลแล้ว เริ่มใหม่ได้เลย! 🚀");
    }
  });
}
init();
</script>
</body>
</html>
