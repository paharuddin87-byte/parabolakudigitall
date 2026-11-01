<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#14264a">
<title>ParabolaKu – Grafik Fungsi Kuadrat</title>
<style>
:root{--bg:#e9ebef;--card:#f7f8fa;--ink:#1a2233;--mut:#5a6478;--pri:#1f3a68;--pri2:#14264a;--acc:#7a1f2f;--ok:#2f6f52;--bad:#b3243b;--line:#cfd4dc;--grid:#dde1e8;--ax:#3a4663;--on-pri:#ffffff;--on-acc:#ffffff;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0d1730;--card:#15213e;--ink:#e8ebf2;--mut:#a6afc3;--pri:#a9bff0;--pri2:#1b2e5a;--acc:#b5465a;--ok:#6fcf9b;--bad:#f08c9a;--line:#2a3960;--grid:#1f2d4d;--ax:#a6afc3;--on-pri:#0d1730;--on-acc:#ffffff;}}
:root[data-theme="dark"]{--bg:#0d1730;--card:#15213e;--ink:#e8ebf2;--mut:#a6afc3;--pri:#a9bff0;--pri2:#1b2e5a;--acc:#b5465a;--ok:#6fcf9b;--bad:#f08c9a;--line:#2a3960;--grid:#1f2d4d;--ax:#a6afc3;--on-pri:#0d1730;--on-acc:#ffffff;}
*{box-sizing:border-box}html,body{height:auto}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.55 "Segoe UI",system-ui,-apple-system,Roboto,sans-serif}
header{background:var(--pri2);color:#f1f3f7;padding:14px 16px 10px;border-bottom:3px solid var(--acc)}
header h1{margin:0;font-size:1.25rem;letter-spacing:.2px}header p{margin:2px 0 0;font-size:.85rem;opacity:.85}
nav{display:flex;gap:6px;overflow-x:auto;padding:8px 12px;background:var(--card);border-bottom:1px solid var(--line);position:sticky;top:env(safe-area-inset-top,0px);z-index:5}
nav button{flex:0 0 auto;border:1px solid var(--line);background:transparent;color:var(--ink);padding:8px 13px;border-radius:999px;font:inherit;font-size:.9rem;cursor:pointer}
nav button.on{background:var(--pri);border-color:var(--pri);color:var(--on-pri);font-weight:600}
main{max-width:920px;margin:0 auto;padding:16px 14px 60px}
section{display:none}section.on{display:block}
h2{margin:.2rem 0 .6rem;font-size:1.35rem}h3{margin:1.1rem 0 .3rem;font-size:1.05rem;color:var(--pri)}
.card{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:14px 16px;margin:12px 0}
.tag{display:inline-block;font-size:.72rem;font-weight:700;letter-spacing:.5px;text-transform:uppercase;background:var(--acc);color:var(--on-acc);border-radius:6px;padding:2px 8px}
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:12px}
@media(max-width:680px){.grid2{grid-template-columns:1fr}}
.btn{background:var(--pri);color:var(--on-pri);border:0;border-radius:10px;padding:10px 16px;font:inherit;font-weight:600;cursor:pointer}
.btn.sec{background:transparent;color:var(--pri);border:1.5px solid var(--pri)}
.btn:disabled{opacity:.45;cursor:default}
.f{font-family:Cambria,"Times New Roman",serif;font-size:1.1em;background:var(--grid);border-radius:8px;padding:8px 12px;display:inline-block;margin:4px 0}
canvas{width:100%;height:auto;background:var(--card);border:1px solid var(--line);border-radius:12px;touch-action:none;display:block}
.sl{display:grid;grid-template-columns:34px 1fr 54px;align-items:center;gap:8px;margin:6px 0}
.sl label{font-weight:700;font-family:Cambria,serif}input[type=range]{width:100%;accent-color:var(--pri)}
.sl output{font-variant-numeric:tabular-nums;text-align:right;font-weight:600}
table{border-collapse:collapse;width:100%;font-size:.93rem}td,th{border:1px solid var(--line);padding:6px 9px;text-align:left}th{background:var(--grid)}
.info td:first-child{color:var(--mut);width:48%}
.opt{display:block;width:100%;text-align:left;margin:6px 0;padding:10px 12px;border:1.5px solid var(--line);background:var(--card);color:var(--ink);border-radius:10px;font:inherit;cursor:pointer}
.opt.ok{border-color:var(--ok);background:color-mix(in srgb,var(--ok) 16%,var(--card))}.opt.bad{border-color:var(--bad);background:color-mix(in srgb,var(--bad) 14%,var(--card))}
.fb{margin-top:8px;padding:9px 12px;border-radius:10px;background:var(--grid);display:none}.fb.show{display:block}
.bar{height:8px;background:var(--grid);border-radius:99px;overflow:hidden;margin:8px 0}.bar i{display:block;height:100%;background:var(--pri);width:0;transition:width .3s}
.steps li{margin:6px 0}.steps li.done{color:var(--ok);font-weight:600}
.big{font-size:2.2rem;font-weight:800;color:var(--pri)}
footer{text-align:center;color:var(--mut);font-size:.8rem;padding:20px 12px}

/* PENGEMBANG */
.dev{max-width:560px;margin:0 auto}
.dev-card{background:var(--card);border:1px solid var(--line);border-radius:22px;overflow:hidden;box-shadow:0 10px 30px rgba(0,0,0,.10)}
.dev-banner{height:120px;position:relative;background:linear-gradient(135deg,var(--pri2),var(--pri) 62%,var(--acc))}
.dev-banner svg{position:absolute;inset:0;width:100%;height:100%}
.avatar{width:152px;height:152px;border-radius:50%;margin:-76px auto 0;position:relative;overflow:hidden;border:5px solid var(--card);box-shadow:0 0 0 3px var(--pri),0 8px 20px rgba(0,0,0,.28);background:linear-gradient(135deg,var(--pri2),var(--acc));display:flex;align-items:center;justify-content:center;color:#fff;font-size:2.8rem;font-weight:800;letter-spacing:1px}
.avatar img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;border-radius:50%;display:block}
.dev-body{padding:14px 20px 24px;text-align:center}
.dev-body h2{margin:.55rem 0 .3rem;font-size:1.55rem;line-height:1.25}
.dev-list{margin-top:20px;display:grid;gap:10px;text-align:left}
.dev-item{display:flex;gap:12px;align-items:center;background:var(--bg);border:1px solid var(--line);border-radius:14px;padding:10px 14px}
.dev-ico{flex:0 0 40px;height:40px;border-radius:12px;background:color-mix(in srgb,var(--pri) 16%,var(--card));display:flex;align-items:center;justify-content:center;font-size:1.15rem}
.dev-item small{display:block;color:var(--mut);font-size:.72rem;font-weight:700;text-transform:uppercase;letter-spacing:.6px}
.dev-item b{display:block;font-variant-numeric:tabular-nums;word-break:break-word}
.dev-note{margin-top:16px;color:var(--mut);font-size:.85rem}

/* HEADER TOMBOL */
header.hdr{display:flex;justify-content:space-between;align-items:center;gap:10px}
.hb{display:flex;gap:8px;flex:0 0 auto}
.hb button{width:42px;height:42px;border-radius:50%;border:1.5px solid rgba(255,255,255,.65);background:rgba(255,255,255,.14);color:#fff;font-size:1.15rem;line-height:1;cursor:pointer}
.hb button:active{transform:scale(.93)}
/* SPLASH */
body.lock{overflow:hidden}
#splash{position:fixed;inset:0;z-index:1000;display:flex;align-items:center;justify-content:center;color:#fff;background:#14264a;overflow:hidden;transition:opacity .5s,visibility .5s;padding:env(safe-area-inset-top,0px) env(safe-area-inset-right,0px) env(safe-area-inset-bottom,0px) env(safe-area-inset-left,0px)}
#splash.out{opacity:0;visibility:hidden}
.sp-bg{position:absolute;inset:0;background-size:cover;background-position:center}
.sp-bg svg{width:100%;height:100%;display:block}
.sp-shade{position:absolute;inset:0;background:linear-gradient(180deg,rgba(8,16,36,.30),rgba(8,16,36,.80))}
.sp-box{position:relative;z-index:1;width:min(92vw,460px);text-align:center;padding:16px}
.sp-logo{width:88px;height:88px;margin:0 auto 10px;border-radius:50%;border:3px solid rgba(255,255,255,.85);background:rgba(255,255,255,.12);display:flex;align-items:center;justify-content:center;backdrop-filter:blur(4px)}
.sp-logo svg{width:52px;height:52px}
.sp-t{margin:0;font-size:2.4rem;font-weight:800;letter-spacing:.5px;text-shadow:0 3px 14px rgba(0,0,0,.4)}
.sp-s{margin:4px 0 22px;font-size:.95rem;opacity:.92}
.sp-row{display:flex;justify-content:space-between;align-items:center;font-size:.85rem;margin-bottom:6px;gap:10px}
.sp-st{display:flex;align-items:center;gap:8px}
.sp-spin{width:14px;height:14px;border-radius:50%;border:2px solid rgba(255,255,255,.35);border-top-color:#fff;animation:spin .8s linear infinite}
.sp-spin.off{display:none}
@keyframes spin{to{transform:rotate(360deg)}}
.sp-track{height:10px;border-radius:99px;background:rgba(255,255,255,.22);overflow:hidden}
.sp-fill{height:100%;width:0;border-radius:99px;background:linear-gradient(90deg,#a82f45,#d9dde5)}
.sp-btn{margin-top:22px;min-width:190px;padding:14px 34px;border:0;border-radius:999px;background:#e9ebef;color:#5e1522;font:inherit;font-weight:800;font-size:1.1rem;letter-spacing:.6px;cursor:pointer;box-shadow:0 8px 22px rgba(0,0,0,.35);transition:transform .15s,opacity .3s}
.sp-btn:disabled{opacity:.4;cursor:default}
.sp-btn:not(:disabled):active{transform:scale(.95)}
.sp-btn.ready{animation:pulse 1.6s ease-in-out infinite}
@keyframes pulse{0%,100%{box-shadow:0 8px 22px rgba(0,0,0,.35),0 0 0 0 rgba(233,235,239,.55)}50%{box-shadow:0 8px 22px rgba(0,0,0,.35),0 0 0 12px rgba(233,235,239,0)}}
.sp-rot{display:none;margin-top:16px;font-size:.82rem;opacity:.92;align-items:center;justify-content:center;gap:10px}
.sp-rot i{display:inline-block;width:16px;height:26px;border:2px solid #fff;border-radius:4px;animation:rot 2.4s ease-in-out infinite}
@keyframes rot{0%,30%{transform:rotate(0)}60%,100%{transform:rotate(-90deg)}}
@media (orientation:portrait) and (pointer:coarse){.sp-rot{display:flex}}
@media (max-height:480px){.sp-box{padding:6px}.sp-logo{width:56px;height:56px;margin-bottom:4px}.sp-logo svg{width:34px;height:34px}.sp-t{font-size:1.8rem}.sp-s{margin:2px 0 12px;font-size:.85rem}.sp-btn{margin-top:12px;padding:10px 28px}}
</style>
<link rel="manifest" href="manifest.webmanifest">
<link rel="icon" type="image/png" href="icons/icon-192.png">
<link rel="apple-touch-icon" href="icons/apple-touch-icon.png">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-title" content="ParabolaKu">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<style>.net{font-size:.7rem;padding:3px 9px;border-radius:99px;border:1px solid rgba(255,255,255,.45);margin-right:6px;white-space:nowrap;color:#fff}.net.off{background:#b3243b;border-color:#b3243b}#idn input{padding:8px;border:1px solid var(--line);border-radius:8px;background:var(--card);color:var(--ink);font:inherit;margin:4px 6px 4px 0;max-width:100%}</style>
</head>
<body class="lock">
<div id="splash" role="dialog" aria-label="Layar pembuka ParabolaKu">
<div class="sp-bg" id="spBg"><svg viewBox="0 0 800 450" preserveAspectRatio="xMidYMid slice" aria-hidden="true"><defs><linearGradient id="spg" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#14264a"/><stop offset=".6" stop-color="#1f3a68"/><stop offset="1" stop-color="#7a1f2f"/></linearGradient></defs><rect width="800" height="450" fill="url(#spg)"/><path d="M0 75H800M0 150H800M0 225H800M0 300H800M0 375H800M100 0V450M200 0V450M300 0V450M400 0V450M500 0V450M600 0V450M700 0V450" stroke="rgba(255,255,255,.10)" stroke-width="1" fill="none"/><path d="M0 340H800M400 0V450" stroke="rgba(255,255,255,.35)" stroke-width="2" fill="none"/><path d="M0 420Q400 -200 800 420" fill="none" stroke="rgba(255,255,255,.55)" stroke-width="5"/><path d="M0 450Q400 -80 800 450" fill="none" stroke="rgba(255,255,255,.28)" stroke-width="3" stroke-dasharray="10 9"/><circle cx="400" cy="110" r="9" fill="#d9dde5"/><circle cx="148" cy="340" r="6" fill="#fff"/><circle cx="652" cy="340" r="6" fill="#fff"/></svg></div>
<div class="sp-shade"></div>
<div class="sp-box">
<div class="sp-logo"><svg viewBox="0 0 52 52" aria-hidden="true"><path d="M6 46Q26 -14 46 46" fill="none" stroke="#fff" stroke-width="4" stroke-linecap="round"/><circle cx="26" cy="16" r="4" fill="#d9dde5"/></svg></div>
<h1 class="sp-t">ParabolaKu</h1>
<p class="sp-s">Grafik Fungsi Kuadrat · Matematika Fase E · Kelas X</p>
<div class="sp-row"><span class="sp-st"><i class="sp-spin" id="spSpin"></i><span id="spSt">Menyiapkan…</span></span><b id="spPct">0%</b></div>
<div class="sp-track" role="progressbar" aria-valuemin="0" aria-valuemax="100" aria-valuenow="0" id="spTrack"><div class="sp-fill" id="spBar"></div></div>
<button class="sp-btn" id="spGo" disabled>Mulai</button>
<div class="sp-rot"><i></i><span>Putar perangkat ke mode landscape untuk tampilan terbaik</span></div>
</div>
</div>
<header class="hdr"><div><h1>ParabolaKu · Grafik Fungsi Kuadrat</h1><p>Matematika Fase E · Kelas X · Eksplorasi, latihan, dan kuis interaktif</p></div><div class="hb"><span id="net" class="net" role="status"></span><button id="snd" data-nosfx="1" aria-label="Suara">🔊</button><button id="rstAll" data-nosfx="1" title="Reset semua" aria-label="Reset semua">↺</button></div></header>
<nav id="nav"></nav>
<main>

<section id="beranda">
<h2>Selamat datang! 👋</h2>
<div class="card"><span class="tag">Masalah</span>
<p>Banyak murid hanya menghafal rumus titik puncak dan sumbu simetri tanpa memahami <b>mengapa</b> bentuk parabola berubah ketika nilai <i>a</i>, <i>b</i>, dan <i>c</i> berubah. Akibatnya, mereka kesulitan menggambar grafik dan menafsirkan masalah nyata.</p>
<span class="tag">Tujuan Pembelajaran</span>
<ul><li>Menjelaskan pengaruh <i>a</i>, <i>b</i>, <i>c</i> dan diskriminan terhadap bentuk grafik fungsi kuadrat.</li>
<li>Menentukan titik potong, sumbu simetri, dan titik puncak.</li>
<li>Menggambar sketsa grafik <i>y = ax² + bx + c</i> secara runtut.</li>
<li>Menyelesaikan masalah kontekstual berkaitan dengan nilai maksimum/minimum.</li></ul></div>
<div class="grid2">
<div class="card"><b>Alur belajar</b><ol><li>Baca <b>Konsep</b></li><li>Bereksperimen di <b>Eksplorasi</b></li><li>Ikuti <b>Langkah Melukis</b></li><li>Coba <b>Latihan</b></li><li>Terapkan di <b>Masalah Nyata</b></li><li>Uji diri di <b>Kuis Akhir</b></li></ol></div>
<div class="card"><b>Mulai dari mana?</b><p>Jika baru pertama kali, mulai dari menu <b>Konsep</b>. Jika sudah paham, langsung ke <b>Kuis Akhir</b>.</p><button class="btn" data-go="konsep">Mulai belajar →</button></div></div>
</section>

<section id="konsep">
<h2>Konsep Dasar</h2>
<div class="card"><h3>Bentuk umum</h3><span class="f">f(x) = ax² + bx + c, &nbsp;a ≠ 0</span>
<p>Grafiknya berbentuk <b>parabola</b>. Unsur-unsur pentingnya:</p>
<table><tr><th>Unsur</th><th>Rumus</th><th>Makna</th></tr>
<tr><td>Diskriminan</td><td>D = b² − 4ac</td><td>D&gt;0: memotong sumbu-x di 2 titik; D=0: menyinggung; D&lt;0: tidak memotong</td></tr>
<tr><td>Sumbu simetri</td><td>x = −b/(2a)</td><td>Garis yang membagi parabola menjadi dua bagian sama</td></tr>
<tr><td>Titik puncak</td><td>(−b/2a , −D/4a)</td><td>Nilai minimum (a&gt;0) atau maksimum (a&lt;0)</td></tr>
<tr><td>Titik potong sumbu-y</td><td>(0 , c)</td><td>Nilai fungsi saat x = 0</td></tr>
<tr><td>Titik potong sumbu-x</td><td>x = (−b ± √D)/2a</td><td>Akar-akar persamaan kuadrat</td></tr></table></div>
<div class="card"><h3>Pengaruh koefisien</h3><ul>
<li><b>a</b>: tanda menentukan arah buka (a&gt;0 ke atas, a&lt;0 ke bawah); |a| besar membuat parabola makin sempit.</li>
<li><b>b</b>: bersama <i>a</i> menentukan letak sumbu simetri.</li>
<li><b>c</b>: titik potong dengan sumbu-y.</li></ul>
<button class="btn" data-go="eksplor">Coba sendiri di Eksplorasi →</button></div>
</section>

<section id="eksplor">
<h2>Eksplorasi Grafik</h2>
<p>Geser slider dan amati perubahan grafik serta unsur-unsurnya.</p>
<canvas id="cv" width="760" height="460"></canvas>
<div class="card">
<div class="sl"><label>a</label><input type="range" id="sa" min="-5" max="5" step="0.5" value="1"><output id="oa"></output></div>
<div class="sl"><label>b</label><input type="range" id="sb" min="-10" max="10" step="0.5" value="-2"><output id="ob"></output></div>
<div class="sl"><label>c</label><input type="range" id="sc" min="-10" max="10" step="0.5" value="-3"><output id="oc"></output></div>
<div id="fx" class="f"></div>
<table class="info" id="inf"></table><button class="btn sec" id="rstEx" data-nosfx="1" style="margin-top:10px">↺ Reset</button></div>
<div class="card"><b>Tantangan:</b> <span id="tant"></span> <button class="btn sec" id="nt" style="margin-top:6px">Tantangan lain</button></div>
</section>

<section id="langkah">
<h2>Langkah Melukis Grafik</h2>
<p>Masukkan fungsi, lalu ikuti langkah-langkahnya satu per satu.</p>
<div class="card"><div class="sl" style="grid-template-columns:34px 1fr 54px"><label>a</label><input type="number" id="la" value="1" step="0.5"><span></span></div>
<div class="sl" style="grid-template-columns:34px 1fr 54px"><label>b</label><input type="number" id="lb" value="-4" step="0.5"><span></span></div>
<div class="sl" style="grid-template-columns:34px 1fr 54px"><label>c</label><input type="number" id="lc" value="3" step="0.5"><span></span></div>
<button class="btn" id="lgo">Mulai</button> <button class="btn sec" id="lrnd">Contoh acak</button> <button class="btn sec" id="lrst" data-nosfx="1">↺ Reset</button></div>
<div class="grid2"><div><canvas id="cv2" width="520" height="400"></canvas></div>
<div class="card"><ol class="steps" id="stp"></ol><div id="stx"></div><button class="btn" id="lnext" disabled>Langkah berikutnya</button></div></div>
</section>

<section id="latihan">
<h2>Latihan Bertingkat</h2>
<p>Soal dibuat acak, jadi kamu bisa berlatih berulang kali. Pilih tingkat kesulitan:</p>
<div style="display:flex;gap:8px;flex-wrap:wrap"><button class="btn sec" data-lv="1">Dasar</button><button class="btn sec" data-lv="2">Menengah</button><button class="btn sec" data-lv="3">Tantangan</button><button class="btn sec" id="rstLat" data-nosfx="1">↺ Reset</button></div>
<div class="card" id="lat" style="display:none"></div>
</section>

<section id="nyata">
<h2>Masalah Nyata: Lintasan Bola</h2>
<div class="card"><p>Bola ditendang dari tanah. Tinggi bola (meter) setelah <i>t</i> detik: <span class="f">h(t) = −5t² + v·t</span>, dengan <i>v</i> kecepatan awal (m/s). Atur <i>v</i> lalu jawab pertanyaan.</p>
<div class="sl"><label>v</label><input type="range" id="sv" min="4" max="30" step="1" value="10"><output id="ov"></output></div>
<canvas id="cv3" width="760" height="320"></canvas>
<table class="info" id="inf3"></table></div>
<div class="card"><b>Pertanyaan:</b> Berapa kecepatan awal agar bola mencapai tinggi maksimum <b>20 m</b>? <div style="margin-top:8px"><input type="number" id="ans3" placeholder="v = ... m/s" style="padding:8px;border-radius:8px;border:1.5px solid var(--line);background:var(--card);color:var(--ink);font:inherit;width:140px"> <button class="btn" id="chk3" data-nosfx="1">Periksa</button> <button class="btn sec" id="rst3" data-nosfx="1">↺ Reset</button></div><div class="fb" id="fb3"></div></div>
</section>

<section id="kuis">
<h2>Kuis Akhir</h2>
<p>Bank soal berisi 30 soal. Setiap kali kuis dimulai, 10 soal ditampilkan secara acak. Dinyatakan tuntas jika skor ≥ 75.</p>
<div style="margin-bottom:8px"><button class="btn sec" id="rstKz" data-nosfx="1">↺ Reset kuis</button></div><div id="kq"></div>
</section>

<section id="pengembang">
<h2>Pengembang</h2>
<div class="dev"><div class="dev-card">
<div class="dev-banner"><svg viewBox="0 0 400 120" preserveAspectRatio="none" aria-hidden="true"><path d="M0 110 Q200 -70 400 110" fill="none" stroke="rgba(255,255,255,.35)" stroke-width="3"/><path d="M0 120 Q200 -30 400 120" fill="none" stroke="rgba(255,255,255,.2)" stroke-width="2" stroke-dasharray="6 6"/></svg></div>
<div class="avatar" role="img" aria-label="Foto profil Paharuddin, S.Pd."><span>PS</span><img src="data:image/jpeg;base64,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" alt="Foto profil Paharuddin, S.Pd." onerror="this.style.display='none'"></div>
<div class="dev-body">
<span class="tag">Pengembang Aplikasi</span>
<h2>Paharuddin, S.Pd.</h2>
<div class="dev-list">
<div class="dev-item"><div class="dev-ico">🪪</div><div><small>NIP</small><b>198707082023211018</b></div></div>
<div class="dev-item"><div class="dev-ico">🏫</div><div><small>Satuan Pendidikan</small><b>SMA Negeri 22 Bone</b></div></div>
</div>
<p class="dev-note">ParabolaKu dikembangkan untuk pembelajaran Grafik Fungsi Kuadrat, Matematika Fase E · Kelas X.</p>
</div></div></div>
</section>
</main>
<footer>ParabolaKu · dibuat untuk pembelajaran Matematika Fase E · semua grafik digambar langsung di peramban, tanpa aset eksternal</footer>

<script>
const $=s=>document.querySelector(s),$$=s=>[...document.querySelectorAll(s)];
const fmt=n=>{const r=Math.round(n*100)/100;return String(r).replace(".",",").replace("-","−")};
const poly=(a,b,c)=>{let s="";const t=(v,p)=>{if(v===0)return;const ab=Math.abs(v),co=(ab===1&&p)?"":fmt(ab);s+=(s===""?(v<0?"−":""):(v<0?" − ":" + "))+co+p};t(a,"x²");t(b,"x");t(c,"");return s||"0"};
function an(a,b,c){const D=b*b-4*a*c,xp=-b/(2*a),yp=c-b*b/(4*a);let r=[];if(D>0)r=[(-b-Math.sqrt(D))/(2*a),(-b+Math.sqrt(D))/(2*a)].sort((p,q)=>p-q);else if(D===0)r=[xp];return{D,xp,yp,r}}
function css(v){return getComputedStyle(document.documentElement).getPropertyValue(v).trim()}
function draw(cv,fn,o){const W=cv.width,H=cv.height,g=cv.getContext("2d");o=Object.assign({x0:-10,x1:10,y0:-10,y1:10,pts:[],axisX:null},o);
const X=x=>(x-o.x0)/(o.x1-o.x0)*W,Y=y=>H-(y-o.y0)/(o.y1-o.y0)*H;g.clearRect(0,0,W,H);
g.lineWidth=1;g.strokeStyle=css("--grid");g.fillStyle=css("--mut");g.font="12px sans-serif";g.beginPath();
const sx=o.sx||Math.max(1,Math.round((o.x1-o.x0)/10)),sy=o.sy||Math.max(1,Math.round((o.y1-o.y0)/10));
for(let x=Math.ceil(o.x0/sx)*sx;x<=o.x1;x+=sx){g.moveTo(X(x),0);g.lineTo(X(x),H)}for(let y=Math.ceil(o.y0/sy)*sy;y<=o.y1;y+=sy){g.moveTo(0,Y(y));g.lineTo(W,Y(y))}g.stroke();
g.strokeStyle=css("--ax");g.lineWidth=1.6;g.beginPath();const ax=Math.min(Math.max(0,o.x0),o.x1),ay=Math.min(Math.max(0,o.y0),o.y1);g.moveTo(0,Y(ay));g.lineTo(W,Y(ay));g.moveTo(X(ax),0);g.lineTo(X(ax),H);g.stroke();
for(let x=Math.ceil(o.x0/sx)*sx;x<=o.x1;x+=sx)if(x)g.fillText(x,X(x)+2,Y(ay)+13);for(let y=Math.ceil(o.y0/sy)*sy;y<=o.y1;y+=sy)if(y)g.fillText(y,X(ax)+4,Y(y)-3);
if(o.axisX!==null){g.setLineDash([7,5]);g.strokeStyle=css("--acc");g.lineWidth=1.8;g.beginPath();g.moveTo(X(o.axisX),0);g.lineTo(X(o.axisX),H);g.stroke();g.setLineDash([])}
g.strokeStyle=css("--pri");g.lineWidth=3;g.beginPath();let st=false;for(let i=0;i<=W;i+=2){const x=o.x0+i/W*(o.x1-o.x0),y=fn(x);if(y<o.y0-50||y>o.y1+50){st=false;continue}st?g.lineTo(i,Y(y)):g.moveTo(i,Y(y));st=true}g.stroke();
o.pts.forEach(p=>{g.fillStyle=css(p.c||"--acc");g.beginPath();g.arc(X(p.x),Y(p.y),6,0,7);g.fill();g.fillStyle=css("--ink");g.font="bold 12px sans-serif";if(p.l)g.fillText(p.l,X(p.x)+8,Y(p.y)-8)})}

/* EFEK SUARA */
let mute=false;try{mute=localStorage.getItem("pk_mute")==="1"}catch(e){}
let AC_=null;
function ctx(){try{const AC=window.AudioContext||window.webkitAudioContext;if(!AC)return null;if(!AC_)AC_=new AC();if(AC_.state==="suspended")AC_.resume();return AC_}catch(e){return null}}
function nada(seq,tipe,vol){const ac=ctx();if(!ac||mute)return;const t=ac.currentTime;seq.forEach(([f,d,l])=>{const o=ac.createOscillator(),g=ac.createGain();o.type=tipe||"triangle";o.frequency.setValueAtTime(f,t+d);o.connect(g);g.connect(ac.destination);g.gain.setValueAtTime(0,t+d);g.gain.linearRampToValueAtTime(vol||.2,t+d+.015);g.gain.exponentialRampToValueAtTime(.001,t+d+l);o.start(t+d);o.stop(t+d+l+.02)})}
const sfx={klik:()=>nada([[880,0,.07]],"square",.07),benar:()=>nada([[659.25,0,.12],[880,.1,.22]],"triangle",.25),salah:()=>nada([[220,0,.18],[165,.14,.3]],"sawtooth",.14),selesai:()=>nada([[523.25,0,.15],[659.25,.12,.15],[783.99,.24,.15],[1046.5,.36,.45]],"triangle",.25),reset:()=>nada([[784,0,.08],[523.25,.08,.08],[392,.16,.18]],"sine",.22)};
document.addEventListener("click",e=>{const b=e.target.closest("button");if(!b||b.closest("#splash")||b.classList.contains("opt")||b.dataset.nosfx)return;sfx.klik()},true);
function sndUI(){const b=$("#snd");b.textContent=mute?"🔇":"🔊";b.title=mute?"Suara mati":"Suara menyala";b.setAttribute("aria-pressed",String(!mute))}
$("#snd").onclick=()=>{mute=!mute;try{localStorage.setItem("pk_mute",mute?"1":"0")}catch(e){}sndUI();if(!mute)sfx.klik()};sndUI();

/* NAV */
const menu=[["beranda","Beranda"],["konsep","Konsep"],["eksplor","Eksplorasi"],["langkah","Langkah Melukis"],["latihan","Latihan"],["nyata","Masalah Nyata"],["kuis","Kuis Akhir"],["pengembang","Pengembang"]];
$("#nav").innerHTML=menu.map(m=>`<button data-go="${m[0]}">${m[1]}</button>`).join("");
function go(id){$$("section").forEach(s=>s.classList.toggle("on",s.id===id));$$("#nav button").forEach(b=>b.classList.toggle("on",b.dataset.go===id));scrollTo(0,0);if(id==="eksplor")ex();if(id==="nyata")rl();if(id==="kuis"&&!kz.started)kzStart()}
document.addEventListener("click",e=>{const t=e.target.closest("[data-go]");if(t)go(t.dataset.go)});

/* EKSPLORASI */
const T=[["Buat parabola terbuka ke bawah dengan titik puncak di atas sumbu-x.","a<0&&an(a,b,c).yp>0"],["Buat parabola yang menyinggung sumbu-x (D = 0).","an(a,b,c).D===0"],["Buat parabola yang tidak memotong sumbu-x dan terbuka ke atas.","a>0&&an(a,b,c).D<0"],["Buat sumbu simetri tepat di x = 2.","an(a,b,c).xp===2"]];
let ti=0,a=1,b=-2,c=-3,tOk=false;
function ex(){a=+$("#sa").value;b=+$("#sb").value;c=+$("#sc").value;if(a===0){a=0.5;$("#sa").value=0.5}
$("#oa").value=fmt(a);$("#ob").value=fmt(b);$("#oc").value=fmt(c);const r=an(a,b,c);
const pts=[{x:r.xp,y:r.yp,l:"Puncak ("+fmt(r.xp)+", "+fmt(r.yp)+")",c:"--bad"},{x:0,y:c,l:"(0, "+fmt(c)+")",c:"--ok"}];r.r.forEach(x=>pts.push({x,y:0,l:fmt(x),c:"--ok"}));
draw($("#cv"),x=>a*x*x+b*x+c,{x0:-10,x1:10,y0:-10,y1:10,pts,axisX:r.xp});
$("#fx").textContent="f(x) = "+poly(a,b,c);
$("#inf").innerHTML=`<tr><td>Arah buka</td><td>${a>0?"ke atas (minimum)":"ke bawah (maksimum)"}</td></tr><tr><td>Diskriminan D</td><td>${fmt(r.D)} → ${r.D>0?"memotong sumbu-x di 2 titik":r.D===0?"menyinggung sumbu-x":"tidak memotong sumbu-x"}</td></tr><tr><td>Sumbu simetri</td><td>x = ${fmt(r.xp)}</td></tr><tr><td>Titik puncak</td><td>(${fmt(r.xp)}, ${fmt(r.yp)})</td></tr><tr><td>Potong sumbu-y</td><td>(0, ${fmt(c)})</td></tr><tr><td>Potong sumbu-x</td><td>${r.r.length?r.r.map(x=>"("+fmt(x)+", 0)").join(" dan "):"tidak ada"}</td></tr>`;
const okT=!!eval(T[ti][1]);if(okT&&!tOk)sfx.benar();tOk=okT;$("#tant").innerHTML=T[ti][0]+(okT?" <b style='color:var(--ok)'>✔ Berhasil!</b>":"")}
["sa","sb","sc"].forEach(i=>$("#"+i).addEventListener("input",ex));$("#nt").onclick=()=>{ti=(ti+1)%T.length;tOk=false;ex()};

/* LANGKAH */
let ls=0,lf=[1,-4,3];
const LS=[
 f=>`Arah buka: a = ${fmt(f[0])} ${f[0]>0?"> 0, parabola terbuka ke atas":"< 0, parabola terbuka ke bawah"}.`,
 f=>{const r=an(...f);return `Hitung D = b² − 4ac = ${fmt(f[1])}² − 4(${fmt(f[0])})(${fmt(f[2])}) = ${fmt(r.D)}. ${r.D>0?"D > 0, ada dua titik potong sumbu-x.":r.D===0?"D = 0, parabola menyinggung sumbu-x.":"D < 0, tidak memotong sumbu-x."}`},
 f=>{const r=an(...f);return `Sumbu simetri: x = −b/(2a) = ${fmt(-f[1])}/${fmt(2*f[0])} = ${fmt(r.xp)}.`},
 f=>{const r=an(...f);return `Titik puncak: (${fmt(r.xp)}, ${fmt(r.yp)}) — nilai ${f[0]>0?"minimum":"maksimum"} fungsi adalah ${fmt(r.yp)}.`},
 f=>{const r=an(...f);return `Titik potong sumbu-y: (0, ${fmt(f[2])}). Sumbu-x: ${r.r.length?r.r.map(x=>"("+fmt(x)+", 0)").join(" dan "):"tidak ada"}.`},
 f=>`Hubungkan semua titik dengan kurva mulus. Grafik f(x) = ${poly(...f)} selesai! 🎉`];
function lk(){const f=lf,r=an(...f);const pts=[];if(ls>=4)pts.push({x:r.xp,y:r.yp,l:"Puncak",c:"--bad"});if(ls>=5){pts.push({x:0,y:f[2],c:"--ok"});r.r.forEach(x=>pts.push({x,y:0,c:"--ok"}))}
const o={x0:-8,x1:8,y0:-8,y1:8,pts,axisX:ls>=3?r.xp:null};
const cv=$("#cv2");if(ls>=6)draw(cv,x=>f[0]*x*x+f[1]*x+f[2],o);else{draw(cv,()=>1e9,o);if(ls>=6)0}
$("#stp").innerHTML=LS.slice(0,ls).map(s=>`<li class="done">${s(f)}</li>`).join("");$("#lnext").disabled=ls>=6;$("#lnext").textContent=ls>=5?"Gambar kurva":"Langkah berikutnya"}
$("#lgo").onclick=()=>{lf=[+$("#la").value||1,+$("#lb").value||0,+$("#lc").value||0];if(!+$("#la").value)$("#la").value=1;ls=0;$("#lnext").disabled=false;lk();$("#stx").textContent="f(x) = "+poly(...lf)};
$("#lnext").onclick=()=>{ls++;lk();if(ls>=6)sfx.selesai()};
$("#lrnd").onclick=()=>{const R=(m)=>Math.floor(Math.random()*(2*m+1))-m;let A=R(2)||1;$("#la").value=A;$("#lb").value=R(6);$("#lc").value=R(6);$("#lgo").click()};

/* SOAL ACAK */
const rnd=(m)=>{let v=0;while(!v)v=Math.floor(Math.random()*(2*m+1))-m;return v};
function gen(lv){let A=rnd(lv===1?2:3),B=rnd(lv===1?4:6),C=rnd(6);const r=an(A,B,C),f=poly(A,B,C);
const kind=lv===1?["arah","sumbuy"][Math.floor(Math.random()*2)]:lv===2?["sumbu","diskr","puncak"][Math.floor(Math.random()*3)]:["maks","akar"][Math.floor(Math.random()*2)];
let q,ans,wr=[];
if(kind==="arah"){q=`Grafik f(x) = ${f} terbuka ke …`;ans=A>0?"atas":"bawah";wr=[A>0?"bawah":"atas","kiri","kanan"]}
else if(kind==="sumbuy"){q=`Titik potong grafik f(x) = ${f} dengan sumbu-y adalah …`;ans=`(0, ${fmt(C)})`;wr=[`(${fmt(C)}, 0)`,`(0, ${fmt(B)})`,`(0, ${fmt(-C)})`]}
else if(kind==="sumbu"){q=`Persamaan sumbu simetri grafik f(x) = ${f} adalah …`;ans=`x = ${fmt(r.xp)}`;wr=[`x = ${fmt(-r.xp)}`,`x = ${fmt(-B/A)}`,`x = ${fmt(r.xp+1)}`]}
else if(kind==="diskr"){q=`Grafik f(x) = ${f} … sumbu-x.`;ans=r.D>0?"memotong di dua titik":r.D===0?"menyinggung":"tidak memotong";wr=["memotong di dua titik","menyinggung","tidak memotong"].filter(x=>x!==ans)}
else if(kind==="puncak"){q=`Titik puncak grafik f(x) = ${f} adalah …`;ans=`(${fmt(r.xp)}, ${fmt(r.yp)})`;wr=[`(${fmt(-r.xp)}, ${fmt(r.yp)})`,`(${fmt(r.xp)}, ${fmt(-r.yp)})`,`(${fmt(r.yp)}, ${fmt(r.xp)})`]}
else if(kind==="maks"){q=`Nilai ${A>0?"minimum":"maksimum"} fungsi f(x) = ${f} adalah …`;ans=fmt(r.yp);wr=[fmt(r.xp),fmt(-r.yp),fmt(C)]}
else{A=1;const p=rnd(5),qq=rnd(5);B=-(p+qq);C=p*qq;q=`Akar-akar dari f(x) = ${poly(A,B,C)} adalah …`;const s=[p,qq].sort((x,y)=>x-y);ans=`${fmt(s[0])} dan ${fmt(s[1])}`;wr=[`${fmt(-s[0])} dan ${fmt(-s[1])}`,`${fmt(s[0])} dan ${fmt(-s[1])}`,`${fmt(p+qq)} dan ${fmt(p*qq)}`]}
wr=[...new Set(wr)].filter(x=>x!==ans).slice(0,3);const opts=[ans,...wr].sort(()=>Math.random()-.5);
const ex=kind==="arah"?"Arah buka ditentukan tanda a.":kind==="sumbuy"?"Titik potong sumbu-y adalah (0, c).":kind==="diskr"?`D = ${fmt(r.D)}.`:kind==="akar"?"Faktorkan: cari dua bilangan yang berjumlah −b dan berkali c.":`Gunakan x = −b/2a = ${fmt(r.xp)} dan y = f(x) = ${fmt(r.yp)}.`;
return{q,ans,opts,ex}}
function ask(box,item,cb){box.innerHTML=`<p><b>${item.q}</b></p>`+item.opts.map(o=>`<button class="opt">${o}</button>`).join("")+`<div class="fb"></div>`;let done=false;
$$("#"+box.id+" .opt").forEach(bt=>bt.onclick=()=>{if(done)return;done=true;const ok=bt.textContent===item.ans;sfx[ok?"benar":"salah"]();bt.classList.add(ok?"ok":"bad");if(!ok)$$("#"+box.id+" .opt").find(x=>x.textContent===item.ans).classList.add("ok");
const fb=$("#"+box.id+" .fb");fb.classList.add("show");fb.innerHTML=(ok?"✔ Tepat! ":"✘ Belum tepat. ")+item.ex;cb(ok)})}
let lvl=1;
function nextQ(){const bx=$("#lat");ask(bx,gen(lvl),()=>{bx.insertAdjacentHTML("beforeend",`<button class="btn" id="nq" style="margin-top:8px">Soal berikutnya →</button>`);$("#nq").onclick=nextQ})}
$$("[data-lv]").forEach(b=>b.onclick=()=>{lvl=+b.dataset.lv;$("#lat").style.display="block";nextQ()});

/* MASALAH NYATA */
function rl(){const v=+$("#sv").value;$("#ov").value=v;const tm=v/10,hm=v*v/20,tt=v/5;
draw($("#cv3"),t=>-5*t*t+v*t,{x0:0,x1:6.5,y0:-2,y1:48,sx:1,sy:5,pts:[{x:tm,y:hm,l:"maks "+fmt(hm)+" m",c:"--bad"},{x:tt,y:0,l:"mendarat",c:"--ok"}],axisX:tm});
$("#inf3").innerHTML=`<tr><td>Fungsi</td><td>h(t) = −5t² + ${v}t</td></tr><tr><td>Waktu mencapai puncak</td><td>t = −b/2a = ${fmt(tm)} detik</td></tr><tr><td>Tinggi maksimum</td><td>${fmt(hm)} m</td></tr><tr><td>Waktu mendarat</td><td>${fmt(tt)} detik</td></tr>`}
$("#sv").addEventListener("input",rl);
$("#chk3").onclick=()=>{const f=$("#fb3");f.classList.add("show");const v=+$("#ans3").value;sfx[v===20?"benar":"salah"]();f.innerHTML=v===20?"✔ Benar! Tinggi maksimum = v²/20 = 400/20 = 20 m.":`Belum tepat. Tinggi maksimum = −D/4a = v²/20. Atur slider dan amati tinggi maksimumnya, lalu cari v yang membuat nilainya 20.`};

/* KUIS */
/* BANK SOAL KUIS (30 soal; jawaban benar selalu di indeks 0, lalu diacak saat ditampilkan) */
const BANK=[{"q":"Grafik fungsi f(x) = −2x² + 5x − 3 terbuka ke …","o":["bawah","atas","kiri","kanan"],"e":"Koefisien a = −2 (negatif), sehingga parabola terbuka ke bawah."},{"q":"Nilai diskriminan dari f(x) = x² − 6x + 5 adalah …","o":["16","56","−16","4"],"e":"D = b² − 4ac = (−6)² − 4(1)(5) = 36 − 20 = 16."},{"q":"Persamaan sumbu simetri grafik f(x) = x² − 6x + 5 adalah …","o":["x = 3","x = −3","x = 6","x = 5"],"e":"x = −b/(2a) = −(−6)/(2·1) = 3."},{"q":"Titik puncak grafik f(x) = x² − 6x + 5 adalah …","o":["(3, −4)","(−3, −4)","(3, 4)","(−4, 3)"],"e":"x = 3, y = f(3) = 9 − 18 + 5 = −4, sehingga titik puncaknya (3, −4)."},{"q":"Titik potong grafik f(x) = 2x² − 3x + 7 dengan sumbu-y adalah …","o":["(0, 7)","(7, 0)","(0, −3)","(0, 2)"],"e":"Saat x = 0, f(0) = c = 7, sehingga titiknya (0, 7)."},{"q":"Akar-akar persamaan kuadrat x² − 5x + 6 = 0 adalah …","o":["2 dan 3","−2 dan −3","1 dan 6","−1 dan −6"],"e":"x² − 5x + 6 = (x − 2)(x − 3) = 0, sehingga x = 2 atau x = 3."},{"q":"Banyak titik potong grafik f(x) = x² + 4x + 4 dengan sumbu-x adalah …","o":["1","0","2","3"],"e":"D = 16 − 16 = 0, sehingga grafik menyinggung sumbu-x di satu titik, yaitu (−2, 0)."},{"q":"Grafik f(x) = x² + 2x + 5 …","o":["tidak memotong sumbu-x dan seluruhnya berada di atas sumbu-x","memotong sumbu-x di dua titik","menyinggung sumbu-x","tidak memotong sumbu-x dan seluruhnya berada di bawah sumbu-x"],"e":"D = 4 − 20 = −16 (negatif) dan a = 1 (positif), sehingga grafik tidak memotong sumbu-x dan seluruhnya di atas sumbu-x."},{"q":"Nilai minimum fungsi f(x) = x² − 4x + 7 adalah …","o":["3","−3","2","7"],"e":"Puncak di x = 2, f(2) = 4 − 8 + 7 = 3. Karena a positif, 3 adalah nilai minimum."},{"q":"Nilai maksimum fungsi f(x) = −x² + 6x − 5 adalah …","o":["4","3","−4","5"],"e":"Puncak di x = 3, f(3) = −9 + 18 − 5 = 4. Karena a negatif, 4 adalah nilai maksimum."},{"q":"Persamaan sumbu simetri grafik f(x) = 2x² + 8x − 1 adalah …","o":["x = −2","x = 2","x = −4","x = 4"],"e":"x = −b/(2a) = −8/(2·2) = −2."},{"q":"Titik puncak grafik f(x) = −x² + 4x + 1 adalah …","o":["(2, 5)","(−2, 5)","(2, −5)","(4, 1)"],"e":"x = −4/(2·(−1)) = 2, f(2) = −4 + 8 + 1 = 5, sehingga puncaknya (2, 5)."},{"q":"Grafik fungsi kuadrat mempunyai titik puncak (1, −4) dan melalui titik (0, −3). Fungsi tersebut adalah …","o":["f(x) = x² − 2x − 3","f(x) = x² + 2x − 3","f(x) = −x² + 2x − 3","f(x) = x² − 2x + 3"],"e":"Bentuk puncak: f(x) = a(x − 1)² − 4. Melalui (0, −3): a − 4 = −3, sehingga a = 1. Jadi f(x) = (x − 1)² − 4 = x² − 2x − 3."},{"q":"Fungsi kuadrat dengan a = 1 yang grafiknya memotong sumbu-x di x = 1 dan x = 4 adalah …","o":["f(x) = x² − 5x + 4","f(x) = x² + 5x + 4","f(x) = x² − 3x + 4","f(x) = x² − 5x − 4"],"e":"f(x) = (x − 1)(x − 4) = x² − 5x + 4."},{"q":"Agar grafik f(x) = x² − 4x + k menyinggung sumbu-x, nilai k adalah …","o":["4","−4","16","2"],"e":"Menyinggung berarti D = 0: 16 − 4k = 0, sehingga k = 4."},{"q":"Agar grafik f(x) = x² + kx + 9 menyinggung sumbu-x, nilai k yang memenuhi adalah …","o":["k = 6 atau k = −6","k = 3 atau k = −3","k = 6 saja","k = 9 atau k = −9"],"e":"D = k² − 36 = 0, sehingga k² = 36 dan k = 6 atau k = −6."},{"q":"Grafik fungsi kuadrat terbuka ke bawah dan mempunyai diskriminan positif (D > 0). Pernyataan yang benar adalah …","o":["puncak berada di atas sumbu-x dan grafik memotong sumbu-x di dua titik","puncak berada di bawah sumbu-x dan grafik tidak memotong sumbu-x","seluruh grafik berada di atas sumbu-x","grafik menyinggung sumbu-x di satu titik"],"e":"Nilai ekstrem = −D/(4a). Karena D positif dan a negatif, nilainya positif (puncak di atas sumbu-x). D positif berarti dua titik potong dengan sumbu-x."},{"q":"Dibandingkan grafik y = x², grafik y = 3x² berbentuk …","o":["lebih sempit","lebih lebar","terbuka ke bawah","sama persis"],"e":"Semakin besar |a|, parabola semakin sempit. Karena |3| lebih besar dari |1|, grafik y = 3x² lebih sempit dan tetap terbuka ke atas."},{"q":"Grafik y = (x − 3)² + 2 diperoleh dari grafik y = x² dengan menggeser …","o":["3 satuan ke kanan dan 2 satuan ke atas","3 satuan ke kiri dan 2 satuan ke atas","3 satuan ke kanan dan 2 satuan ke bawah","3 satuan ke kiri dan 2 satuan ke bawah"],"e":"Bentuk y = (x − p)² + q berpuncak di (p, q) = (3, 2): geser 3 ke kanan dan 2 ke atas."},{"q":"Titik puncak grafik f(x) = 2(x + 1)² − 5 adalah …","o":["(−1, −5)","(1, −5)","(−1, 5)","(1, 5)"],"e":"Bentuk f(x) = a(x − p)² + q berpuncak di (p, q). Karena (x + 1) = (x − (−1)), puncaknya (−1, −5)."},{"q":"Daerah hasil (range) fungsi f(x) = x² − 2x + 3 adalah …","o":["{y | y ≥ 2, y ∈ ℝ}","{y | y ≤ 2, y ∈ ℝ}","{y | y ≥ 1, y ∈ ℝ}","{y | y ≥ 3, y ∈ ℝ}"],"e":"Puncak di x = 1, f(1) = 1 − 2 + 3 = 2. Karena a positif, nilai terkecil fungsi adalah 2, sehingga y ≥ 2."},{"q":"Daerah hasil (range) fungsi f(x) = −x² + 4x adalah …","o":["{y | y ≤ 4, y ∈ ℝ}","{y | y ≥ 4, y ∈ ℝ}","{y | y ≤ 2, y ∈ ℝ}","{y | y ≤ −4, y ∈ ℝ}"],"e":"Puncak di x = 2, f(2) = −4 + 8 = 4. Karena a negatif, nilai terbesar fungsi adalah 4, sehingga y ≤ 4."},{"q":"Hasil kali akar-akar persamaan 2x² − 6x + 4 = 0 adalah …","o":["2","3","4","−2"],"e":"Akar-akarnya x = 1 dan x = 2, sehingga hasil kalinya 2. (Sesuai rumus c/a = 4/2 = 2.)"},{"q":"Titik potong grafik f(x) = x² − x − 6 dengan sumbu-x adalah …","o":["(3, 0) dan (−2, 0)","(−3, 0) dan (2, 0)","(6, 0) dan (−1, 0)","(3, 0) dan (2, 0)"],"e":"x² − x − 6 = (x − 3)(x + 2) = 0, sehingga x = 3 atau x = −2."},{"q":"Tinggi sebuah bola (meter) setelah t detik dinyatakan oleh h(t) = −5t² + 20t. Tinggi maksimum bola adalah …","o":["20 meter","40 meter","10 meter","15 meter"],"e":"Waktu mencapai puncak t = −20/(2·(−5)) = 2 detik, h(2) = −20 + 40 = 20 meter."},{"q":"Sebuah persegi panjang mempunyai keliling 40 m. Luas maksimum persegi panjang tersebut adalah …","o":["100 m²","80 m²","75 m²","120 m²"],"e":"Jika panjang x, lebar 20 − x. Luas L = x(20 − x) = −x² + 20x, maksimum di x = 10 dengan L = 100 m²."},{"q":"Keuntungan suatu usaha dinyatakan oleh P(x) = −x² + 10x − 16 (dalam ribuan rupiah) dengan x banyak barang. Usaha tidak untung dan tidak rugi (P = 0) ketika x = …","o":["2 dan 8","−2 dan −8","1 dan 16","5 dan 16"],"e":"−x² + 10x − 16 = 0 sama dengan x² − 10x + 16 = 0, atau (x − 2)(x − 8) = 0, sehingga x = 2 atau x = 8."},{"q":"Grafik fungsi kuadrat melalui titik (0, 5), (1, 2), dan (2, 1). Fungsi tersebut adalah …","o":["f(x) = x² − 4x + 5","f(x) = x² + 4x + 5","f(x) = −x² + 4x + 5","f(x) = 2x² − 6x + 5"],"e":"Dari (0, 5): c = 5. Dari (1, 2): a + b = −3. Dari (2, 1): 4a + 2b = −4, atau 2a + b = −2. Selisihnya a = 1, lalu b = −4. Jadi f(x) = x² − 4x + 5."},{"q":"Grafik fungsi kuadrat memotong sumbu-x di titik (−1, 0) dan (5, 0). Persamaan sumbu simetrinya adalah …","o":["x = 2","x = 3","x = 4","x = −2"],"e":"Sumbu simetri berada di tengah kedua titik potong: x = (−1 + 5)/2 = 2."},{"q":"Agar grafik f(x) = x² − 2x + c tidak memotong sumbu-x, nilai c harus memenuhi …","o":["c > 1","c lebih kecil dari 1","c ≥ 1","c > 4"],"e":"Tidak memotong berarti D negatif: 4 − 4c kurang dari 0, sehingga c > 1."}];
const kocok=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a};
const SOAL_KUIS=10;
const buatSoal=s=>({q:s.q,ans:s.o[0],opts:kocok(s.o),ex:s.e});

const kz={started:false,i:0,s:0,q:[]};
function kzStart(){kz.started=true;kz.i=0;kz.s=0;kz.q=kocok(BANK).slice(0,SOAL_KUIS).map(buatSoal);kzShow()}
function kzShow(){const bx=$("#kq");if(kz.i>=kz.q.length){const p=Math.round(kz.s/kz.q.length*100);sfx[p>=75?"selesai":"salah"]();try{kirimHasil(p)}catch(e){}bx.innerHTML=`<div class="card"><div class="big">${p}</div><p>Skor akhir kamu (${kz.s} dari ${kz.q.length} benar).</p><p>${p>=75?"Hebat! Kamu sudah mencapai ketuntasan (≥ 75). Coba ulangi dengan soal baru untuk menjaga kemampuanmu.":"Belum mencapai 75. Ulangi menu Konsep, Eksplorasi, dan Latihan, lalu coba kuis lagi dengan soal baru."}</p><button class="btn" id="rk">Ulangi kuis</button></div>`;$("#rk").onclick=kzStart;return}
bx.innerHTML=`<div class="bar"><i style="width:${kz.i/kz.q.length*100}%"></i></div><small>Soal ${kz.i+1} dari ${kz.q.length}</small><div class="card" id="kc"></div>`;
ask($("#kc"),kz.q[kz.i],ok=>{if(ok)kz.s++;$("#kc").insertAdjacentHTML("beforeend",`<button class="btn" id="kn" style="margin-top:8px">${kz.i+1<kz.q.length?"Lanjut →":"Lihat skor"}</button>`);$("#kn").onclick=()=>{kz.i++;kzShow()}})}

/* RESET */
function resetEx(){$("#sa").value=1;$("#sb").value=-2;$("#sc").value=-3;ti=0;tOk=false;ex()}
function resetLk(){$("#la").value=1;$("#lb").value=-4;$("#lc").value=3;ls=0;lf=[1,-4,3];lk();$("#stx").textContent="";$("#lnext").disabled=true}
function resetLat(){const l=$("#lat");l.style.display="none";l.innerHTML="";lvl=1}
function reset3(){$("#sv").value=10;$("#ans3").value="";const f=$("#fb3");f.classList.remove("show");f.innerHTML="";rl()}
$("#rstEx").onclick=()=>{resetEx();sfx.reset()};
$("#lrst").onclick=()=>{resetLk();sfx.reset()};
$("#rstLat").onclick=()=>{resetLat();sfx.reset()};
$("#rst3").onclick=()=>{reset3();sfx.reset()};
$("#rstKz").onclick=()=>{kzStart();sfx.reset()};
$("#rstAll").onclick=()=>{resetEx();resetLk();resetLat();reset3();kzStart();go("beranda");sfx.reset()};

go("beranda");

/* SPLASH SCREEN */
const SPLASH_BG=""; // placeholder gambar latar: isi dengan data URI gambar (data:image/jpeg;base64,...)
(function(){
const sp=$("#splash"),bar=$("#spBar"),pct=$("#spPct"),st=$("#spSt"),spin=$("#spSpin"),btn=$("#spGo"),trk=$("#spTrack");
if(SPLASH_BG){const bg=$("#spBg");bg.style.backgroundImage='url("'+SPLASH_BG+'")';bg.querySelector("svg").style.display="none"}
const msgs=[[0,"Menyiapkan grafik…"],[35,"Memuat materi…"],[70,"Menyusun latihan…"],[100,"Siap digunakan!"]];
const D=2600,t0=performance.now();
const iv=setInterval(()=>{const x=Math.min(1,(performance.now()-t0)/D),v=Math.round((1-Math.pow(1-x,1.6))*100);
bar.style.width=v+"%";pct.textContent=v+"%";trk.setAttribute("aria-valuenow",v);
st.textContent=msgs.filter(m=>v>=m[0]).pop()[1];
if(x>=1){clearInterval(iv);spin.classList.add("off");btn.disabled=false;btn.classList.add("ready");btn.focus({preventScroll:true})}},40);
function bunyi(){try{const AC=window.AudioContext||window.webkitAudioContext;if(!AC)return;const ac=new AC(),t=ac.currentTime;
[[523.25,0],[783.99,.09],[1046.5,.18]].forEach(([f,d])=>{const o=ac.createOscillator(),g=ac.createGain();o.type="triangle";o.frequency.value=f;o.connect(g);g.connect(ac.destination);
g.gain.setValueAtTime(0,t+d);g.gain.linearRampToValueAtTime(.25,t+d+.02);g.gain.exponentialRampToValueAtTime(.001,t+d+.28);o.start(t+d);o.stop(t+d+.3)});
setTimeout(()=>{try{ac.close()}catch(e){}},900)}catch(e){}}
function layarPenuh(){
const hp=matchMedia("(pointer:coarse)").matches&&Math.min(screen.width,screen.height)<900;if(!hp)return;
const el=document.documentElement,rq=el.requestFullscreen||el.webkitRequestFullscreen;
const kunci=()=>{try{const o=screen.orientation;if(o&&o.lock)o.lock("landscape").catch(()=>{})}catch(e){}};
try{const r=rq&&rq.call(el);if(r&&r.then)r.then(kunci).catch(()=>{});else kunci()}catch(e){}}
btn.onclick=()=>{bunyi();layarPenuh();sp.classList.add("out");document.body.classList.remove("lock");scrollTo(0,0);setTimeout(()=>sp.remove(),600)};
})();
matchMedia("(prefers-color-scheme: dark)").addEventListener("change",()=>{ex();rl();lk()});

/* ONLINE/OFFLINE, PWA, DAN SINKRONISASI HASIL KUIS (opsional) */
const SYNC_URL=""; // Isi dengan URL Web App Apps Script (berakhiran /exec) agar hasil kuis masuk ke Google Sheets. Kosong = fitur nonaktif.
(function(){
const net=$("#net");
function antri(){try{return JSON.parse(localStorage.getItem("pk_q")||"[]")}catch(e){return[]}}
function simpan(a){try{localStorage.setItem("pk_q",JSON.stringify(a))}catch(e){}}
let busy=false;
async function flush(){if(!SYNC_URL||busy||!navigator.onLine)return;busy=true;const a=antri();try{while(a.length){await fetch(SYNC_URL,{method:"POST",mode:"no-cors",headers:{"Content-Type":"text/plain;charset=utf-8"},body:JSON.stringify(a[0])});a.shift();simpan(a)}}catch(e){}busy=false}
function status(){const on=navigator.onLine;net.textContent=on?"● Online":"○ Offline";net.classList.toggle("off",!on);if(on)flush()}
addEventListener("online",status);addEventListener("offline",status);status();
window.kirimHasil=function(p){if(!SYNC_URL)return;const g=i=>(($("#"+i)||{}).value||"").trim().slice(0,60);
const a=antri();a.push({id:Date.now()+"-"+Math.random().toString(36).slice(2,7),nama:g("idNama"),kelas:g("idKelas"),skor:p,benar:kz.s,total:kz.q.length,waktu:new Date().toISOString()});simpan(a);flush()};
if(SYNC_URL){const kq=$("#kq");let n="",k="";try{n=localStorage.getItem("pk_n")||"";k=localStorage.getItem("pk_k")||""}catch(e){}
kq.insertAdjacentHTML("beforebegin",'<div class="card" id="idn"><b>Identitas siswa</b><br><input id="idNama" placeholder="Nama" autocomplete="name"><input id="idKelas" placeholder="Kelas"></div>');
$("#idNama").value=n;$("#idKelas").value=k;
$("#idn").addEventListener("input",()=>{try{localStorage.setItem("pk_n",$("#idNama").value);localStorage.setItem("pk_k",$("#idKelas").value)}catch(e){}})}
if("serviceWorker" in navigator&&/^https?:$/.test(location.protocol)&&!/googleusercontent|script\.google/.test(location.hostname)){addEventListener("load",()=>{navigator.serviceWorker.register("sw.js").catch(()=>{})})}
})();
</script>
</body>
</html>
