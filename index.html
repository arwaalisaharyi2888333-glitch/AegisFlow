<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AegisFlow — النموذج الأولي التفاعلي لإدارة الفعاليات</title>
  <style>
    :root {
      --bg: #0f172a;
      --panel: #1e293b;
      --panel-2: #0b1120;
      --text: #f8fafc;
      --muted: #94a3b8;
      --accent: #38bdf8;
      --accent-2: #818cf8;
      --ok: #22c55e;
      --warn: #f59e0b;
      --danger: #ef4444;
      --border: rgba(148, 163, 184, 0.18);
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: system-ui, -apple-system, "Segoe UI", Tahoma, sans-serif;
      background: linear-gradient(135deg, var(--bg), var(--panel-2));
      color: var(--text);
      min-height: 100vh;
    }
    header {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      padding: 16px 24px;
      background: rgba(15, 23, 42, 0.85);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      backdrop-filter: blur(8px);
      z-index: 10;
    }
    .brand { display: flex; align-items: center; gap: 10px; }
    .brand-badge {
      width: 36px; height: 36px; border-radius: 10px;
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      display: grid; place-items: center; font-weight: 800; color: #09111e;
    }
    .brand h1 { margin: 0; font-size: 1.15rem; }
    .brand span { font-size: 0.8rem; color: var(--muted); }
    .toolbar { display: flex; flex-wrap: wrap; gap: 8px; }
    button {
      cursor: pointer;
      border: 1px solid var(--border);
      background: var(--panel);
      color: var(--text);
      padding: 8px 14px;
      border-radius: 8px;
      font-size: 0.88rem;
      transition: 0.15s ease;
    }
    button:hover { border-color: var(--accent); transform: translateY(-1px); }
    button.primary {
      background: var(--accent);
      color: #06131f;
      border: none;
      font-weight: 700;
    }
    .container { max-width: 1200px; margin: 24px auto; padding: 0 20px 40px; }
    .kpis {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 14px;
      margin-bottom: 22px;
    }
    .kpi {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 16px;
    }
    .kpi .label { color: var(--muted); font-size: 0.85rem; }
    .kpi .val { font-size: 1.65rem; font-weight: 800; margin: 6px 0 2px; }
    .kpi .sub { font-size: 0.78rem; color: var(--ok); }
    .grid-2 {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
      gap: 18px;
      margin-bottom: 22px;
    }
    .card {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 18px;
    }
    .card h2 { margin: 0 0 12px; font-size: 1.05rem; }
    .gate-row {
      display: flex; justify-content: space-between; align-items: center;
      padding: 10px 12px; border-radius: 10px;
      background: rgba(15, 23, 42, 0.55); margin-bottom: 10px;
    }
    .pill {
      padding: 3px 10px; border-radius: 999px; font-size: 0.78rem; font-weight: 700;
    }
    .pill.ok { background: rgba(34,197,94,0.18); color: #4ade80; }
    .pill.warn { background: rgba(245,158,11,0.18); color: #fbbf24; }
    .pill.alert { background: rgba(239,68,68,0.18); color: #f87171; }
    .bar-wrap { margin-top: 10px; }
    .bar-bg {
      height: 10px; background: rgba(148,163,184,0.15);
      border-radius: 999px; overflow: hidden; margin-top: 6px;
    }
    .bar-fill {
      height: 100%; width: 68%;
      background: linear-gradient(90deg, var(--accent), var(--ok));
      transition: width 0.35s ease;
    }
    table { width: 100%; border-collapse: collapse; font-size: 0.88rem; }
    th, td { text-align: right; padding: 10px 8px; border-bottom: 1px solid var(--border); }
    th { color: var(--muted); font-weight: 600; }
    .toast {
      position: fixed; bottom: 20px; left: 20px;
      background: var(--accent); color: #06131f;
      padding: 10px 16px; border-radius: 10px; font-weight: 700;
      opacity: 0; transform: translateY(10px); transition: 0.25s ease;
      pointer-events: none;
    }
    .toast.show { opacity: 1; transform: translateY(0); }
  </style>
</head>
<body>
  <header>
    <div class="brand">
      <div class="brand-badge">AF</div>
      <div>
        <h1>AegisFlow — لوحة إدارة الحشود والعمليات</h1>
        <span>نموذج أولي تفاعلي (Interactive Prototype)</span>
      </div>
    </div>
    <div class="toolbar">
      <button class="primary" onclick="simulateTick()">محاكاة تحديث لحظي</button>
      <button onclick="rerouteGate('B')">تحويل مسار البوابة B</button>
      <button onclick="exportReport()">تصدير تقرير الحالة</button>
    </div>
  </header>

  <main class="container">
    <section class="kpis">
      <div class="kpi">
        <div class="label">إجمالي الحضور الحالي</div>
        <div class="val" id="kpi-attendance">4,820</div>
        <div class="sub" id="kpi-delta">+3.4% خلال آخر 10 دقائق</div>
      </div>
      <div class="kpi">
        <div class="label">نسبة الإشغال التشغيلية</div>
        <div class="val" id="kpi-occupancy">68%</div>
        <div class="sub">ضمن الحدود الآمنة</div>
      </div>
      <div class="kpi">
        <div class="label">متوسط زمن العبور</div>
        <div class="val" id="kpi-wait">42 ثانية</div>
        <div class="sub">مؤشر الأداء (KPI) نشط</div>
      </div>
      <div class="kpi">
        <div class="label">البلاغات والفرق الميدانية</div>
        <div class="val" id="kpi-teams">14 / 16</div>
        <div class="sub">جاهزية عالية</div>
      </div>
    </section>

    <section class="grid-2">
      <div class="card">
        <h2>حالة البوابات والمناطق</h2>
        <div class="gate-row">
          <div>
            <strong>البوابة A — المدخل الرئيسي</strong><br />
            <small style="color:var(--muted)">تدفق منتظم • 3 مسارات نشطة</small>
          </div>
          <span class="pill ok" id="gate-a-status">طبيعي</span>
        </div>
        <div class="gate-row">
          <div>
            <strong>البوابة B — الممر الجانبي</strong><br />
            <small style="color:var(--muted)" id="gate-b-note">كثافة متوسطة • جاهز للتحويل</small>
          </div>
          <span class="pill warn" id="gate-b-status">متابعة</span>
        </div>
        <div class="gate-row">
          <div>
            <strong>منطقة الخدمات والطوارئ</strong><br />
            <small style="color:var(--muted)">فرق الإسعاف والتنظيم في مواقعها</small>
          </div>
          <span class="pill ok">جاهز</span>
        </div>
        <div class="bar-wrap">
          <div style="display:flex;justify-content:space-between;font-size:0.85rem;">
            <span>كفاءة توزيع الحشود</span>
            <strong id="eff-label">68%</strong>
          </div>
          <div class="bar-bg"><div class="bar-fill" id="eff-bar"></div></div>
        </div>
      </div>

      <div class="card">
        <h2>سجل القرارات والإجراءات الفورية</h2>
        <table>
          <thead>
            <tr>
              <th>الوقت</th>
              <th>الإجراء / القرار</th>
              <th>الحالة</th>
            </tr>
          </thead>
          <tbody id="log-body">
            <tr>
              <td>22:30</td>
              <td>تفعيل مسار إضافي في البوابة A</td>
              <td><span class="pill ok">منفذ</span></td>
            </tr>
            <tr>
              <td>22:41</td>
              <td>مراجعة كثافة البوابة B وإرسال تنبيه ميداني</td>
              <td><span class="pill warn">قيد المتابعة</span></td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>
  </main>

  <div class="toast" id="toast">تم التحديث</div>

  <script>
    let attendance = 4820;
    let occupancy = 68;
    let gateBRouted = false;

    function showToast(msg) {
      const t = document.getElementById("toast");
      t.textContent = msg;
      t.classList.add("show");
      setTimeout(() => t.classList.remove("show"), 2400);
    }

    function addLog(action, statusText, pillClass) {
      const now = new Date().toTimeString().slice(0, 5);
      const tbody = document.getElementById("log-body");
      const tr = document.createElement("tr");
      tr.innerHTML = `<td>${now}</td><td>${action}</td><td><span class="pill ${pillClass}">${statusText}</span></td>`;
      tbody.prepend(tr);
    }

    function simulateTick() {
      const delta = Math.floor(Math.random() * 140) - 35;
      attendance = Math.max(1000, attendance + delta);
      occupancy = Math.min(95, Math.max(35, occupancy + (delta > 0 ? 2 : -1)));

      document.getElementById("kpi-attendance").textContent = attendance.toLocaleString("en-US");
      document.getElementById("kpi-delta").textContent = `${delta >= 0 ? "+" : ""}${delta} زائر في التحديث الحالي`;
      document.getElementById("kpi-occupancy").textContent = occupancy + "%";
      document.getElementById("eff-label").textContent = occupancy + "%";
      document.getElementById("eff-bar").style.width = occupancy + "%";

      addLog("تحديث بيانات الحساسات ومؤشرات KPI", "محدث", "ok");
      showToast("تم تحديث بيانات النموذج الأولي");
    }

    function rerouteGate(gate) {
      gateBRouted = !gateBRouted;
      const badge = document.getElementById("gate-b-status");
      const note = document.getElementById("gate-b-note");
      if (gateBRouted) {
        badge.textContent = "محوّل";
        badge.className = "pill ok";
        note.textContent = "تم تحويل التدفق وتخفيف الضغط بنجاح";
        occupancy = Math.max(40, occupancy - 5);
        addLog(`إعادة توجيه المسارات للبوابة ${gate}`, "منفذ", "ok");
        showToast(`تم تحويل مسار البوابة ${gate}`);
      } else {
        badge.textContent = "متابعة";
        badge.className = "pill warn";
        note.textContent = "كثافة متوسطة • جاهز للتحويل";
        addLog(`إعادة البوابة ${gate} للوضع الافتراضي`, "متابعة", "warn");
        showToast(`تمت إعادة البوابة ${gate}`);
      }
      document.getElementById("kpi-occupancy").textContent = occupancy + "%";
      document.getElementById("eff-label").textContent = occupancy + "%";
      document.getElementById("eff-bar").style.width = occupancy + "%";
    }

    function exportReport() {
      const summary = `تقرير AegisFlow\nالحضور: ${attendance}\nالإشغال: ${occupancy}%`;
      navigator.clipboard?.writeText(summary).catch(() => {});
      addLog("تصدير ملخص الحالة التشغيلية", "مكتمل", "ok");
      showToast("تم نسخ ملخص التقرير");
    }
  </script>
</body>
</html>
