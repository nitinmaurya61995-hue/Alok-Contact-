


<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Alok — Contact Card</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#080712;
      --glass: rgba(255,255,255,0.04);
      --neon1: #ff2d95;
      --neon2: #33d4ff;
      --neon3: #8a2be2;
      --accent: linear-gradient(90deg,var(--neon1),var(--neon2),var(--neon3));
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      font-family:'Poppins',system-ui,-apple-system,Segoe UI,Roboto,Arial;
      background:
        radial-gradient(600px 300px at 10% 15%, rgba(51,212,255,0.06), transparent),
        radial-gradient(500px 260px at 90% 85%, rgba(255,45,149,0.05), transparent),
        var(--bg);
      color:#eaf8ff;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:28px;
    }

    /* Card */
    .card{
      width:100%;
      max-width:920px;
      border-radius:16px;
      padding:28px;
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      box-shadow: 0 10px 40px rgba(0,0,0,0.6);
      border:1px solid rgba(255,255,255,0.04);
      position:relative;
      overflow:hidden;
    }

    /* Neon strips */
    .neon-strip{
      position:absolute;
      height:220%;
      width:14px;
      right:-40px;
      top:-10%;
      background: var(--accent);
      filter: blur(20px);
      opacity:0.45;
      transform: rotate(22deg);
      pointer-events:none;
    }
    .neon-strip.left{
      left:-40px; right:auto;
      transform: rotate(-22deg);
    }

    .wrap{
      display:flex;
      gap:28px;
      align-items:center;
    }

    /* Left - big name */
    .left{
      flex:1 1 60%;
      padding:10px;
    }
    .badge{
      display:inline-block;
      padding:6px 12px;
      border-radius:999px;
      font-weight:600;
      font-size:13px;
      background: rgba(255,255,255,0.02);
      border:1px solid rgba(255,255,255,0.04);
      color:#dff9ff;
      margin-bottom:12px;
    }
    h1{
      font-size:78px;
      margin:6px 0 8px 0;
      line-height:0.88;
      letter-spacing:2px;
      background: linear-gradient(90deg,var(--neon1),var(--neon2));
      -webkit-background-clip:text;
      background-clip:text;
      color:transparent;
      text-shadow: 0 0 18px rgba(255,45,149,0.16), 0 0 30px rgba(51,212,255,0.08);
    }
    .sub{
      font-size:17px;
      color:#cfefff;
      opacity:0.95;
      margin-bottom:18px;
    }

    /* CTA Buttons */
    .ctas{display:flex; gap:12px; flex-wrap:wrap}
    .btn{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding:10px 16px;
      border-radius:10px;
      cursor:pointer;
      text-decoration:none;
      font-weight:700;
      letter-spacing:0.3px;
      border:1px solid rgba(255,255,255,0.06);
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      color:#e7fbff;
    }
    .btn.primary{
      background: var(--accent);
      color:#06060d;
      box-shadow: 0 10px 30px rgba(51,212,255,0.08);
    }

    /* Right - contacts */
    .right{
      width:320px;
      min-width:240px;
      border-radius:12px;
      padding:16px;
      background: linear-gradient(180deg, rgba(255,255,255,0.016), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.04);
    }
    .avatar{
      height:88px; width:88px; border-radius:50%;
      display:flex; align-items:center; justify-content:center;
      font-weight:800; font-size:26px; color:#05030a;
      background: linear-gradient(135deg,var(--neon2),var(--neon3));
      box-shadow: 0 10px 30px rgba(138,43,226,0.12);
      margin-bottom:12px;
    }
    .meta{font-weight:700; margin-bottom:4px; color:#eaffff}
    .small{font-size:13px; opacity:0.85; margin-bottom:8px}

    .contacts{display:flex; flex-direction:column; gap:10px; margin-top:8px}
    .contact-row{
      display:flex; gap:12px; align-items:center;
      padding:8px 10px; border-radius:10px;
      background: linear-gradient(90deg, rgba(255,255,255,0.008), rgba(255,255,255,0.006));
      border:1px solid rgba(255,255,255,0.028);
      font-weight:600;
    }
    .contact-row a{color:inherit; text-decoration:none}

    .icon{
      width:36px;height:36px;border-radius:8px;display:inline-flex;align-items:center;justify-content:center;
      background: linear-gradient(90deg,var(--neon1),var(--neon2));
      color:#07060a;font-weight:800;
      box-shadow: 0 8px 26px rgba(51,212,255,0.06);
      font-size:14px;
    }

    footer{margin-top:16px;font-size:13px;opacity:0.8;color:#d6f6ff}

    /* responsive */
    @media(max-width:820px){
      .wrap{flex-direction:column; align-items:stretch}
      h1{font-size:48px}
      .right{width:100%}
    }
  </style>
</head>
<body>
  <div class="card" role="main">
    <div class="neon-strip left"></div>
    <div class="neon-strip"></div>

    <div class="wrap">
      <!-- LEFT: Hero -->
      <div class="left">
        <div class="badge">NEON • PERSONAL</div>
        <h1>ALOK</h1>
        <div class="sub">Alok Kurmi — (Akki Bhai)<br>Connect with me on phone & socials 👇</div>

        <div class="ctas" aria-hidden="false">
          <a class="btn primary" href="tel:+917819905018" title="Call Alok">Call: +91 78199 05018</a>
          <a class="btn" href="https://www.instagram.com/alok_kurmi_2.0?igsh=d3VpczlmeHRmOGdt" target="_blank" rel="noopener">Instagram</a>
          <a class="btn" href="https://t.me/Alok_10k" target="_blank" rel="noopener">Telegram</a>
        </div>

        <footer>
          <div style="margin-top:12px">Tip: Click the buttons above to open dialer or open social profiles.</div>
        </footer>
      </div>

      <!-- RIGHT: Contact Card -->
      <aside class="right" aria-label="Contact information">
        <div style="display:flex;align-items:center;gap:12px;">
          <div class="avatar">A</div>
          <div>
            <div class="meta">Alok Kurmi (Akki Bhai)</div>
            <div class="small">Friendly neon creator</div>
          </div>
        </div>

        <div class="contacts" role="list">
          <div class="contact-row" role="listitem">
            <div class="icon">📞</div>
            <div><a href="tel:+917819905018">+91 78199 05018</a></div>
          </div>

          <div class="contact-row" role="listitem">
            <div class="icon">📸</div>
            <div>
              <div style="font-weight:700">Instagram</div>
              <div style="font-size:13px;opacity:0.9"><a href="https://www.instagram.com/alok_kurmi_2.0?igsh=d3VpczlmeHRmOGdt" target="_blank" rel="noopener">@alok_kurmi_2.0</a></div>
            </div>
          </div>

          <div class="contact-row" role="listitem">
            <div class="icon">✈️</div>
            <div>
              <div style="font-weight:700">Telegram</div>
              <div style="font-size:13px;opacity:0.9"><a href="https://t.me/Alok_10k" target="_blank" rel="noopener">@Alok_10k</a></div>
            </div>
          </div>

          <div class="contact-row" role="listitem">
            <div class="icon">f</div>
            <div>
              <div style="font-weight:700">Facebook</div>
              <div style="font-size:13px;opacity:0.9">
                <!-- I don't have exact FB URL — replace this with your real FB profile link if needed -->
                <a href="https://www.facebook.com/alok.kurmi" target="_blank" rel="noopener">/alok.kurmi</a>
              </div>
            </div>
          </div>

          <div class="contact-row" role="listitem">
            <div class="icon">👤</div>
            <div>
              <div style="font-weight:700">Display Name</div>
              <div style="font-size:13px;opacity:0.9">Alok Kurmi (Akki Bhai)</div>
            </div>
          </div>
        </div>
      </aside>
    </div>
  </div>
</body>
</html>
