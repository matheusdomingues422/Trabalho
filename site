<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="theme-color" content="#101012" />
  <title>Brasa & Rua — Hambúrguer • Hot Dog • Bebidas</title>
  <meta name="description" content="Site profissional para vender hambúrguer, cachorro-quente e bebidas. Cardápio, combos, adicionais, carrinho e pedido via WhatsApp." />

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500,700&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      /* Aesthetic: "Street premium" (noir + warm ember) */
      --bg: #0b0b0d;
      --bg2:#101013;
      --ink: #f6f4ef;
      --muted: rgba(246,244,239,.72);
      --muted2: rgba(246,244,239,.52);
      --line: rgba(246,244,239,.12);

      --ember:#ff4d2e;
      --ember2:#ff8a2a;
      --lime:#c8ff6a;   /* for success / availability */
      --ice:#67e8f9;    /* for drinks accents */
      --gold:#f7d38b;   /* subtle highlight */

      --shadow: 0 18px 50px rgba(0,0,0,.55);
      --shadow2: 0 10px 24px rgba(0,0,0,.4);
      --radius: 22px;

      --max: 1200px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Plus Jakarta Sans", system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
      background:
        radial-gradient(1200px 900px at 12% 8%, rgba(255,77,46,.22), transparent 55%),
        radial-gradient(1000px 800px at 88% 14%, rgba(103,232,249,.15), transparent 55%),
        radial-gradient(900px 700px at 60% 98%, rgba(255,138,42,.14), transparent 50%),
        linear-gradient(180deg, var(--bg), var(--bg2));
      color: var(--ink);
      overflow-x:hidden;
    }

    a{color:inherit}
    button,input,select,textarea{font:inherit}
    ::selection{background: rgba(255,77,46,.25)}

    /* Subtle grit texture */
    .grain{
      pointer-events:none;
      position:fixed; inset:0;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='220' height='220'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='220' height='220' filter='url(%23n)' opacity='.22'/%3E%3C/svg%3E");
      mix-blend-mode: overlay;
      opacity:.22;
      z-index:0;
    }

    .wrap{max-width:var(--max); margin:0 auto; padding:0 20px}
    .stack{display:flex; flex-direction:column; gap:14px}
    .row{display:flex; gap:14px; align-items:center}

    /* Topbar */
    header{
      position:sticky; top:0; z-index:50;
      backdrop-filter: blur(14px);
      background: rgba(10,10,12,.55);
      border-bottom: 1px solid rgba(246,244,239,.10);
    }
    .topbar{
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding: 14px 0;
      gap:12px;
    }
    .brand{
      display:flex; align-items:center; gap:12px; min-width: 220px;
    }
    .mark{
      width:40px; height:40px; border-radius: 12px;
      background:
        radial-gradient(12px 12px at 30% 35%, rgba(255,255,255,.18), transparent 60%),
        conic-gradient(from 210deg, var(--ember), var(--ember2), var(--ice), var(--ember));
      box-shadow: 0 10px 30px rgba(255,77,46,.18);
      position:relative;
      overflow:hidden;
    }
    .mark:after{
      content:"";
      position:absolute; inset:-2px;
      background: radial-gradient(80px 60px at 30% 20%, rgba(255,255,255,.16), transparent 60%);
      transform: rotate(12deg);
    }
    .brand h1{
      margin:0;
      font-family:"Fraunces", serif;
      font-weight:700;
      letter-spacing:.2px;
      font-size: 18px;
      line-height:1.1;
    }
    .brand small{
      display:block;
      color: var(--muted2);
      font-weight:600;
      letter-spacing:.12em;
      text-transform:uppercase;
      margin-top:2px;
      font-size: 10px;
    }

    nav{
      display:flex; align-items:center; gap: 14px;
      flex-wrap:wrap;
      justify-content:center;
    }
    nav a{
      text-decoration:none;
      color: var(--muted);
      font-weight:600;
      font-size: 13px;
      letter-spacing:.06em;
      text-transform:uppercase;
      padding:10px 10px;
      border-radius: 999px;
      border: 1px solid transparent;
      transition: .2s ease;
    }
    nav a:hover{
      color: var(--ink);
      border-color: rgba(246,244,239,.16);
      background: rgba(246,244,239,.06);
      transform: translateY(-1px);
    }

    .actions{
      display:flex; align-items:center; justify-content:flex-end;
      gap:10px;
      min-width: 220px;
    }
    .pill{
      display:inline-flex; align-items:center; gap:10px;
      padding: 10px 12px;
      border-radius: 999px;
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.06);
      box-shadow: var(--shadow2);
    }
    .pill .dot{
      width:8px; height:8px; border-radius:99px;
      background: var(--lime);
      box-shadow: 0 0 0 4px rgba(200,255,106,.12);
    }
    .pill span{
      color: var(--muted);
      font-weight:700;
      font-size: 12px;
      letter-spacing:.06em;
      text-transform:uppercase;
      white-space:nowrap;
    }

    .btn{
      border:0;
      cursor:pointer;
      color: var(--ink);
      font-weight:800;
      letter-spacing:.02em;
      padding: 12px 14px;
      border-radius: 14px;
      background:
        radial-gradient(14px 14px at 28% 30%, rgba(255,255,255,.25), transparent 60%),
        linear-gradient(135deg, rgba(255,77,46,1), rgba(255,138,42,1));
      box-shadow: 0 14px 40px rgba(255,77,46,.18);
      transition: transform .15s ease, filter .2s ease, box-shadow .2s ease;
      display:inline-flex; align-items:center; gap:10px;
      white-space:nowrap;
    }
    .btn:hover{transform: translateY(-2px); filter:saturate(1.05); box-shadow: 0 18px 50px rgba(255,77,46,.25);}
    .btn:active{transform: translateY(0px) scale(.98);}

    .btnGhost{
      border:1px solid rgba(246,244,239,.16);
      cursor:pointer;
      color: var(--ink);
      font-weight:800;
      letter-spacing:.02em;
      padding: 12px 14px;
      border-radius: 14px;
      background: rgba(246,244,239,.06);
      box-shadow: var(--shadow2);
      transition: transform .15s ease, background .2s ease, border-color .2s ease;
      display:inline-flex; align-items:center; gap:10px;
      white-space:nowrap;
    }
    .btnGhost:hover{transform: translateY(-2px); background: rgba(246,244,239,.08); border-color: rgba(246,244,239,.22);}
    .btnGhost:active{transform: translateY(0px) scale(.98);}

    .icon{
      width:18px; height:18px; display:inline-block;
    }

    /* Hero */
    main{position:relative; z-index:1}
    .hero{
      padding: 40px 0 22px;
    }
    .heroGrid{
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 22px;
      align-items:stretch;
    }
    .heroLeft{
      border-radius: var(--radius);
      border: 1px solid rgba(246,244,239,.12);
      background:
        radial-gradient(900px 500px at 10% 10%, rgba(255,77,46,.22), transparent 55%),
        radial-gradient(700px 420px at 85% 25%, rgba(103,232,249,.16), transparent 55%),
        linear-gradient(180deg, rgba(246,244,239,.06), rgba(246,244,239,.03));
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
      padding: 26px;
    }
    .heroLeft:before{
      content:"";
      position:absolute; inset:-80px -40px auto auto;
      width: 280px; height: 280px;
      background: conic-gradient(from 90deg, rgba(255,77,46,.0), rgba(255,77,46,.35), rgba(255,138,42,.0));
      filter: blur(10px);
      transform: rotate(-12deg);
    }

    .kicker{
      display:flex; align-items:center; gap:10px; flex-wrap:wrap;
      color: var(--muted);
      font-weight:700;
      letter-spacing:.12em;
      text-transform:uppercase;
      font-size: 12px;
    }
    .kicker .tag{
      border:1px solid rgba(246,244,239,.14);
      padding: 7px 10px;
      border-radius: 999px;
      background: rgba(246,244,239,.06);
    }

    .hero h2{
      font-family:"Fraunces", serif;
      margin: 14px 0 10px;
      font-size: clamp(34px, 4.2vw, 56px);
      line-height: 1.02;
      letter-spacing: -0.02em;
    }
    .hero p{
      margin: 0 0 16px;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.7;
      max-width: 58ch;
    }

    .heroCTA{
      display:flex; gap:10px; flex-wrap:wrap;
      margin-top: 14px;
    }

    .heroMeta{
      display:grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap:10px;
      margin-top: 18px;
    }
    .metaItem{
      border: 1px solid rgba(246,244,239,.12);
      background: rgba(246,244,239,.05);
      border-radius: 16px;
      padding: 12px 12px;
    }
    .metaItem b{
      display:block;
      font-size: 14px;
      letter-spacing:.02em;
    }
    .metaItem span{
      display:block;
      margin-top:6px;
      color: var(--muted2);
      font-weight:600;
      font-size: 12px;
      line-height:1.3;
    }

    .heroRight{
      border-radius: var(--radius);
      border: 1px solid rgba(246,244,239,.12);
      background:
        radial-gradient(500px 320px at 70% 20%, rgba(255,138,42,.25), transparent 56%),
        linear-gradient(180deg, rgba(246,244,239,.06), rgba(246,244,239,.03));
      box-shadow: var(--shadow);
      padding: 18px;
      position:relative;
      overflow:hidden;
    }

    /* Illustrative "food poster" using SVG */
    .poster{
      border-radius: 18px;
      border: 1px solid rgba(246,244,239,.12);
      background: rgba(0,0,0,.22);
      overflow:hidden;
      position:relative;
      min-height: 310px;
    }
    .poster svg{display:block; width:100%; height:auto}
    .posterCaption{
      position:absolute; left:14px; right:14px; bottom:14px;
      display:flex; justify-content:space-between; gap:10px; align-items:flex-end;
    }
    .price{
      font-family:"Fraunces", serif;
      font-size: 28px;
      letter-spacing:-.02em;
    }
    .price small{
      display:block;
      color: var(--muted2);
      font-family:"Plus Jakarta Sans", sans-serif;
      font-size: 12px;
      letter-spacing:.08em;
      text-transform:uppercase;
      margin-top:2px;
      font-weight:700;
    }
    .miniBadge{
      border:1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.06);
      padding: 9px 10px;
      border-radius: 14px;
      color: var(--muted);
      font-weight:800;
      font-size: 12px;
      letter-spacing:.06em;
      text-transform:uppercase;
      max-width: 190px;
    }

    /* Content sections */
    section{padding: 26px 0}
    .sectionHead{
      display:flex; align-items:flex-end; justify-content:space-between; gap:12px;
      margin-bottom: 14px;
    }
    .sectionHead h3{
      margin:0;
      font-family:"Fraunces", serif;
      font-size: clamp(22px, 2.2vw, 30px);
      letter-spacing:-.02em;
    }
    .sectionHead p{
      margin:0;
      color: var(--muted);
      font-weight:600;
      max-width: 60ch;
      line-height:1.6;
      font-size: 13px;
    }

    /* Menu layout (no generic cards; use list rows) */
    .menu{
      border-radius: var(--radius);
      border: 1px solid rgba(246,244,239,.12);
      background: rgba(246,244,239,.04);
      box-shadow: var(--shadow2);
      overflow:hidden;
    }
    .menuToolbar{
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      align-items:center;
      justify-content:space-between;
      padding: 14px 14px;
      border-bottom: 1px solid rgba(246,244,239,.10);
      background: rgba(0,0,0,.22);
    }
    .search{
      display:flex; align-items:center; gap:10px;
      padding: 10px 12px;
      border-radius: 14px;
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.05);
      min-width: min(560px, 100%);
      flex: 1 1 340px;
    }
    .search input{
      width:100%;
      border:0;
      outline:0;
      background: transparent;
      color: var(--ink);
      font-weight:600;
    }
    .search input::placeholder{color: rgba(246,244,239,.45)}
    .filters{
      display:flex; flex-wrap:wrap; gap:8px;
      justify-content:flex-end;
    }
    .chip{
      border:1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.04);
      color: var(--muted);
      padding: 9px 10px;
      border-radius: 999px;
      font-weight:800;
      letter-spacing:.08em;
      text-transform:uppercase;
      font-size: 11px;
      cursor:pointer;
      transition:.2s ease;
      user-select:none;
    }
    .chip:hover{transform: translateY(-1px); background: rgba(246,244,239,.06); border-color: rgba(246,244,239,.22); color: var(--ink)}
    .chip[aria-pressed="true"]{
      color: var(--ink);
      border-color: rgba(255,77,46,.55);
      background: rgba(255,77,46,.14);
      box-shadow: 0 12px 30px rgba(255,77,46,.10);
    }

    .menuGrid{
      display:grid;
      grid-template-columns: 1fr .75fr;
      gap: 0;
      min-height: 420px;
    }

    .menuList{
      padding: 6px 0;
    }
    .menuGroup{
      padding: 10px 14px 6px;
      color: var(--muted2);
      font-weight:900;
      letter-spacing:.16em;
      text-transform:uppercase;
      font-size: 11px;
    }

    .item{
      display:grid;
      grid-template-columns: 1fr auto;
      gap: 12px;
      padding: 12px 14px;
      border-top: 1px solid rgba(246,244,239,.08);
      align-items:center;
    }
    .item:first-of-type{border-top: 0}
    .item:hover{
      background: linear-gradient(90deg, rgba(255,77,46,.08), transparent 60%);
    }
    .itemTitle{
      display:flex; align-items:baseline; gap:10px; flex-wrap:wrap;
    }
    .itemTitle b{
      font-size: 14px;
      letter-spacing:.01em;
    }
    .badges{display:flex; gap:6px; flex-wrap:wrap}
    .badge{
      font-size: 10px;
      font-weight:900;
      letter-spacing:.12em;
      text-transform:uppercase;
      padding: 5px 7px;
      border-radius: 999px;
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.04);
      color: var(--muted);
    }
    .badge.hot{border-color: rgba(255,77,46,.45); background: rgba(255,77,46,.12); color: rgba(255,200,190,.95)}
    .badge.ice{border-color: rgba(103,232,249,.45); background: rgba(103,232,249,.10); color: rgba(205,249,255,.95)}
    .itemDesc{
      margin-top:6px;
      color: var(--muted);
      font-size: 12px;
      line-height:1.55;
      max-width: 72ch;
    }
    .itemRight{
      display:flex; align-items:center; gap:10px;
    }
    .itemPrice{
      font-family:"Fraunces", serif;
      font-size: 16px;
      letter-spacing:-.01em;
      color: var(--ink);
      min-width: 82px;
      text-align:right;
    }
    .addBtn{
      border:1px solid rgba(246,244,239,.16);
      background: rgba(246,244,239,.05);
      color: var(--ink);
      border-radius: 14px;
      padding: 10px 10px;
      cursor:pointer;
      font-weight:900;
      letter-spacing:.06em;
      text-transform:uppercase;
      font-size: 11px;
      display:inline-flex; align-items:center; gap:8px;
      transition: .2s ease;
    }
    .addBtn:hover{
      transform: translateY(-2px);
      border-color: rgba(255,77,46,.45);
      background: rgba(255,77,46,.12);
    }
    .addBtn:active{transform: translateY(0px) scale(.98);}

    /* Cart panel */
    .cart{
      border-left: 1px solid rgba(246,244,239,.10);
      background: rgba(0,0,0,.18);
      padding: 14px;
      display:flex;
      flex-direction:column;
      gap:12px;
    }
    .cartHead{
      display:flex; align-items:flex-end; justify-content:space-between; gap:10px;
    }
    .cartHead h4{
      margin:0;
      font-family:"Fraunces", serif;
      font-size: 20px;
      letter-spacing:-.02em;
    }
    .cartHead span{
      color: var(--muted2);
      font-weight:800;
      letter-spacing:.12em;
      text-transform:uppercase;
      font-size: 11px;
      white-space:nowrap;
    }

    .cartList{
      border: 1px solid rgba(246,244,239,.12);
      border-radius: 18px;
      overflow:hidden;
      background: rgba(246,244,239,.04);
    }
    .cartRow{
      display:grid;
      grid-template-columns: 1fr auto;
      gap: 10px;
      padding: 12px 12px;
      border-top: 1px solid rgba(246,244,239,.08);
    }
    .cartRow:first-child{border-top:0}
    .cartRow b{font-size: 13px}
    .cartRow small{
      display:block;
      margin-top:5px;
      color: var(--muted2);
      font-weight:600;
      line-height:1.4;
    }
    .qty{
      display:flex; align-items:center; gap:8px; justify-content:flex-end;
    }
    .qty button{
      width:34px; height:34px;
      border-radius: 12px;
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.05);
      color: var(--ink);
      cursor:pointer;
      font-weight:900;
      transition: .2s ease;
    }
    .qty button:hover{transform: translateY(-1px); border-color: rgba(246,244,239,.22); background: rgba(246,244,239,.08);}
    .qty button:active{transform: translateY(0px) scale(.98);}
    .qty span{
      min-width: 22px;
      text-align:center;
      font-weight:900;
      color: var(--ink);
    }

    .totals{
      border: 1px solid rgba(246,244,239,.12);
      border-radius: 18px;
      background: rgba(246,244,239,.04);
      padding: 12px;
    }
    .line{
      display:flex; justify-content:space-between; align-items:center;
      color: var(--muted);
      font-weight:700;
      padding: 6px 0;
      font-size: 13px;
    }
    .line strong{
      color: var(--ink);
      font-family:"Fraunces", serif;
      font-size: 16px;
      letter-spacing:-.01em;
    }

    .field{
      display:flex; flex-direction:column; gap:7px;
      border: 1px solid rgba(246,244,239,.12);
      border-radius: 18px;
      background: rgba(246,244,239,.04);
      padding: 12px;
    }
    .field label{
      color: var(--muted2);
      font-weight:900;
      letter-spacing:.12em;
      text-transform:uppercase;
      font-size: 10px;
    }
    .field input, .field textarea, .field select{
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(0,0,0,.16);
      color: var(--ink);
      border-radius: 14px;
      padding: 10px 11px;
      outline:none;
      font-weight:600;
    }
    .field textarea{min-height: 84px; resize: vertical}
    .field input:focus, .field textarea:focus, .field select:focus{
      border-color: rgba(255,77,46,.45);
      box-shadow: 0 0 0 4px rgba(255,77,46,.12);
    }

    .cartActions{
      display:flex; gap:10px; flex-wrap:wrap;
    }
    .cartActions .btn, .cartActions .btnGhost{flex:1}
    .hint{
      color: var(--muted2);
      font-size: 12px;
      line-height:1.5;
      margin: 2px 0 0;
    }

    /* Info band */
    .infoBand{
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap: 18px;
      align-items:stretch;
    }
    .panel{
      border-radius: var(--radius);
      border: 1px solid rgba(246,244,239,.12);
      background: rgba(246,244,239,.04);
      box-shadow: var(--shadow2);
      padding: 18px;
      position:relative;
      overflow:hidden;
    }
    .panel h4{
      margin:0 0 8px;
      font-family:"Fraunces", serif;
      font-size: 22px;
      letter-spacing:-.02em;
    }
    .panel p{margin:0; color: var(--muted); line-height:1.7; font-size: 13px}
    .panel .bullets{
      margin-top:12px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
    }
    .bullet{
      border: 1px solid rgba(246,244,239,.10);
      border-radius: 16px;
      padding: 10px 10px;
      background: rgba(0,0,0,.18);
    }
    .bullet b{display:block; font-size: 13px}
    .bullet span{display:block; margin-top:5px; color: var(--muted2); font-weight:600; font-size: 12px; line-height:1.4}

    /* Footer */
    footer{
      padding: 28px 0 40px;
      border-top: 1px solid rgba(246,244,239,.10);
      background: rgba(0,0,0,.18);
      margin-top: 18px;
    }
    .footGrid{
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:18px;
      align-items:start;
    }
    .fine{
      color: var(--muted2);
      font-size: 12px;
      line-height:1.6;
    }
    .links{
      display:flex; flex-wrap:wrap; gap:10px; justify-content:flex-end;
    }
    .links a{
      text-decoration:none;
      color: var(--muted);
      border: 1px solid rgba(246,244,239,.14);
      background: rgba(246,244,239,.04);
      padding: 10px 12px;
      border-radius: 999px;
      font-weight:800;
      letter-spacing:.08em;
      text-transform:uppercase;
      font-size: 11px;
      transition:.2s ease;
    }
    .links a:hover{
      transform: translateY(-1px);
      color: var(--ink);
      border-color: rgba(246,244,239,.22);
      background: rgba(246,244,239,.07);
    }

    /* Reveal animations */
    .reveal{
      opacity:0;
      transform: translateY(10px);
      animation: fadeUp .8s ease forwards;
    }
    .reveal.d2{animation-delay:.08s}
    .reveal.d3{animation-delay:.16s}
    .reveal.d4{animation-delay:.24s}
    .reveal.d5{animation-delay:.32s}
    @keyframes fadeUp{
      to{opacity:1; transform: translateY(0)}
    }

    /* Responsive */
    @media (max-width: 980px){
      .heroGrid{grid-template-columns: 1fr; }
      .menuGrid{grid-template-columns: 1fr; }
      .cart{border-left:0; border-top: 1px solid rgba(246,244,239,.10)}
      .infoBand{grid-template-columns: 1fr}
      .footGrid{grid-template-columns: 1fr}
      .links{justify-content:flex-start}
      .brand{min-width:auto}
      .actions{min-width:auto}
      nav{display:none}
    }
    @media (max-width: 520px){
      .heroMeta{grid-template-columns: 1fr}
      .panel .bullets{grid-template-columns: 1fr}
      .btn,.btnGhost,.chip,.addBtn,.qty button{transition:none}
      .btn,.btnGhost{width:100%; justify-content:center}
      .actions .pill{display:none}
    }

    /* Reduced motion */
    @media (prefers-reduced-motion: reduce){
      *{scroll-behavior:auto !important}
      .reveal{animation:none; opacity:1; transform:none}
      .btn,.btnGhost,.chip,.addBtn,.qty button{transition:none}
    }
  </style>
</head>

<body>
  <div class="grain" aria-hidden="true"></div>

  <header>
    <div class="wrap topbar">
      <div class="brand" aria-label="Brasa & Rua">
        <div class="mark" aria-hidden="true"></div>
        <div>
          <h1>Brasa & Rua <small>Hambúrguer • Hot Dog • Bebidas</small></h1>
        </div>
      </div>

      <nav aria-label="Navegação principal">
        <a href="#cardapio">Cardápio</a>
        <a href="#combos">Combos</a>
        <a href="#como-funciona">Como funciona</a>
        <a href="#contato">Contato</a>
      </nav>

      <div class="actions">
        <div class="pill" title="Status da cozinha">
          <span class="dot" aria-hidden="true"></span>
          <span id="statusLoja">Aberto agora</span>
        </div>
        <button class="btnGhost" id="btnVerCarrinho" type="button" aria-label="Ver carrinho">
          <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
            <path d="M7 7h14l-2 9H8L7 7Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
            <path d="M7 7 6 3H3" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
            <path d="M9 21a1 1 0 1 0 0-2 1 1 0 0 0 0 2ZM18 21a1 1 0 1 0 0-2 1 1 0 0 0 0 2Z" stroke="currentColor" stroke-width="2"/>
          </svg>
          Carrinho <span id="cartCount" style="opacity:.85; font-weight:900;">(0)</span>
        </button>
      </div>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="wrap heroGrid">
        <article class="heroLeft reveal">
          <div class="kicker">
            <span class="tag">Entrega & Retirada</span>
            <span class="tag">Pedido rápido no WhatsApp</span>
            <span class="tag">Pagamentos: Pix • Cartão</span>
          </div>

          <h2>Seu lanche com <span style="color: var(--gold);">cara de artesanal</span> — <span style="color: var(--ember2);">veloz</span> como comida de rua.</h2>
          <p>
            Monte seu pedido direto no site: escolha hambúrguer ou hot dog, adicione extras e finalize pelo WhatsApp com o resumo certinho.
            Ideal para vender com aparência profissional, sem complicação.
          </p>

          <div class="heroCTA">
            <a class="btn" href="#cardapio">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M4 7h16M4 12h16M4 17h16" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
              Ver cardápio
            </a>
            <button class="btnGhost" id="btnRolagemCombos" type="button">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M12 3v18M7 8l5-5 5 5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" transform="rotate(180 12 12)"/>
              </svg>
              Ver combos
            </button>
          </div>

          <div class="heroMeta">
            <div class="metaItem reveal d2">
              <b>Tempo médio</b>
              <span>20–35 min (varia por região)</span>
            </div>
            <div class="metaItem reveal d3">
              <b>Taxa de entrega</b>
              <span id="taxaEntregaTexto">R$ 7,00 fixa</span>
            </div>
            <div class="metaItem reveal d4">
              <b>Horário</b>
              <span id="horarioTexto">Seg–Dom • 18:00–23:30</span>
            </div>
          </div>
        </article>

        <aside class="heroRight reveal d2" aria-label="Destaque do dia">
          <div class="poster" role="img" aria-label="Ilustração de hambúrguer e hot dog em estilo poster">
            <!-- Inline SVG artwork (no external images) -->
            <svg viewBox="0 0 820 560" xmlns="http://www.w3.org/2000/svg">
              <defs>
                <linearGradient id="g1" x1="0" y1="0" x2="1" y2="1">
                  <stop offset="0" stop-color="#ff4d2e" stop-opacity=".9"/>
                  <stop offset=".55" stop-color="#ff8a2a" stop-opacity=".75"/>
                  <stop offset="1" stop-color="#67e8f9" stop-opacity=".30"/>
                </linearGradient>
                <radialGradient id="g2" cx="30%" cy="30%" r="70%">
                  <stop offset="0" stop-color="#ffffff" stop-opacity=".20"/>
                  <stop offset="1" stop-color="#ffffff" stop-opacity="0"/>
                </radialGradient>
                <filter id="blur" x="-20%" y="-20%" width="140%" height="140%">
                  <feGaussianBlur stdDeviation="18"/>
                </filter>
              </defs>

              <rect x="0" y="0" width="820" height="560" fill="#0b0b0d"/>
              <ellipse cx="210" cy="140" rx="210" ry="140" fill="url(#g1)" filter="url(#blur)" opacity=".75"/>
              <ellipse cx="650" cy="160" rx="200" ry="140" fill="url(#g2)" opacity=".9"/>
              <ellipse cx="540" cy="460" rx="260" ry="140" fill="url(#g1)" filter="url(#blur)" opacity=".35"/>

              <!-- Burger -->
              <g transform="translate(90,175)">
                <path d="M60 140c0-65 75-110 180-110s180 45 180 110c0 12-7 18-18 18H78c-11 0-18-6-18-18z" fill="#f7d38b" opacity=".95"/>
                <path d="M92 110c26-22 82-40 148-40s122 18 148 40" stroke="#dba95a" stroke-width="10" stroke-linecap="round" opacity=".55"/>
                <rect x="78" y="158" width="324" height="26" rx="13" fill="#2a2a2f" opacity=".75"/>

                <rect x="90" y="184" width="300" height="30" rx="12" fill="#7b2f1a" opacity=".95"/>
                <rect x="92" y="208" width="296" height="18" rx="9" fill="#ff4d2e" opacity=".22"/>
                <path d="M100 182h280c-20 22-58 46-140 46s-120-24-140-46z" fill="#4ade80" opacity=".55"/>
                <rect x="78" y="226" width="324" height="46" rx="20" fill="#f7d38b" opacity=".9"/>
                <path d="M120 240c40 10 80 12 120 12s80-2 120-12" stroke="#dba95a" stroke-width="8" stroke-linecap="round" opacity=".45"/>
              </g>

              <!-- Hot dog -->
              <g transform="translate(420,250) rotate(-6)">
                <rect x="60" y="90" width="310" height="70" rx="35" fill="#f7d38b" opacity=".92"/>
                <rect x="96" y="105" width="238" height="40" rx="20" fill="#7b2f1a" opacity=".92"/>
                <path d="M105 125c40-16 70 16 110 0s70 16 110 0" fill="none" stroke="#ff4d2e" stroke-width="10" stroke-linecap="round" opacity=".65"/>
                <path d="M105 132c40-16 70 16 110 0s70 16 110 0" fill="none" stroke="#f7d38b" stroke-width="6" stroke-linecap="round" opacity=".35"/>
              </g>

              <!-- Typography lines -->
              <g opacity=".85">
                <text x="60" y="70" font-size="22" fill="#f6f4ef" font-family="Plus Jakarta Sans, sans-serif" letter-spacing="4">DESTAQUE</text>
                <text x="60" y="108" font-size="44" fill="#f6f4ef" font-family="Fraunces, serif" font-weight="700">Combo Brasa</text>
                <text x="60" y="140" font-size="18" fill="rgba(246,244,239,.75)" font-family="Plus Jakarta Sans, sans-serif" letter-spacing="1">
                  Burger + Hot Dog + Refri (lata)
                </text>
              </g>
            </svg>

            <div class="posterCaption">
              <div class="price">R$ <span id="precoDestaque">34,90</span>
                <small>Preço sugerido • edite como quiser</small>
              </div>
              <div class="miniBadge">Mais vendido da casa</div>
            </div>
          </div>

          <p class="hint" style="margin: 10px 2px 0;">
            Dica: personalize nome, horários, valores e o WhatsApp no botão “Configurar”.
          </p>

          <div class="cartActions" style="margin-top: 10px;">
            <button class="btnGhost" id="btnConfig" type="button" aria-label="Configurar dados da loja">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M12 15.5a3.5 3.5 0 1 0 0-7 3.5 3.5 0 0 0 0 7Z" stroke="currentColor" stroke-width="2"/>
                <path d="M19.4 15a7.97 7.97 0 0 0 .1-1 7.97 7.97 0 0 0-.1-1l2-1.5-2-3.5-2.4 1a7.9 7.9 0 0 0-1.7-1L15 4h-6l-.4 2.5a7.9 7.9 0 0 0-1.7 1l-2.4-1-2 3.5 2 1.5a7.97 7.97 0 0 0-.1 1c0 .34.03.67.1 1l-2 1.5 2 3.5 2.4-1c.52.43 1.1.77 1.7 1L9 20h6l.4-2.5c.6-.23 1.18-.57 1.7-1l2.4 1 2-3.5-2-1.5Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
              </svg>
              Configurar
            </button>
            <button class="btn" id="btnPedirDestaque" type="button" aria-label="Adicionar combo destaque ao carrinho">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M12 5v14M5 12h14" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
              Quero esse combo
            </button>
          </div>
        </aside>
      </div>
    </section>

    <section id="cardapio">
      <div class="wrap">
        <div class="sectionHead reveal">
          <div class="stack" style="gap:6px">
            <h3>Cardápio</h3>
            <p>Itens organizados por categoria. Use a busca e adicione extras no carrinho. Finalize com mensagem pronta no WhatsApp.</p>
          </div>
          <p class="hint" style="text-align:right; margin:0">
            <span style="color: var(--muted2); font-weight:900; letter-spacing:.12em; text-transform:uppercase; font-size:10px;">Atalhos</span><br/>
            Digite “bacon”, “refri”, “hot dog”…
          </p>
        </div>

        <div class="menu reveal d2" aria-label="Área do cardápio e carrinho">
          <div class="menuToolbar">
            <div class="search" role="search" aria-label="Buscar no cardápio">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M10.5 18a7.5 7.5 0 1 0 0-15 7.5 7.5 0 0 0 0 15Z" stroke="currentColor" stroke-width="2"/>
                <path d="M16.5 16.5 21 21" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
              <input id="q" type="search" placeholder="Buscar no cardápio (ex.: smash, cheddar, ketchup, coca)..." autocomplete="off" />
            </div>

            <div class="filters" aria-label="Filtros">
              <button class="chip" data-filter="todos" aria-pressed="true" type="button">Todos</button>
              <button class="chip" data-filter="burger" aria-pressed="false" type="button">Hambúrguer</button>
              <button class="chip" data-filter="hotdog" aria-pressed="false" type="button">Hot dog</button>
              <button class="chip" data-filter="bebida" aria-pressed="false" type="button">Bebidas</button>
              <button class="chip" data-filter="extra" aria-pressed="false" type="button">Extras</button>
            </div>
          </div>

          <div class="menuGrid">
            <div class="menuList" id="menuList" aria-label="Lista de itens do cardápio">
              <!-- JS renders items -->
            </div>

            <aside class="cart" id="carrinho" aria-label="Carrinho de compras">
              <div class="cartHead">
                <h4>Seu pedido</h4>
                <span id="cartMini">0 itens</span>
              </div>

              <div class="cartList" id="cartList" aria-live="polite">
                <!-- JS renders cart -->
              </div>

              <div class="totals" aria-label="Totais do pedido">
                <div class="line"><span>Subtotal</span><strong id="subtotal">R$ 0,00</strong></div>
                <div class="line"><span>Entrega</span><strong id="entrega">R$ 0,00</strong></div>
                <div class="line" style="border-top:1px solid rgba(246,244,239,.10); margin-top:6px; padding-top:10px;">
                  <span>Total</span><strong id="total">R$ 0,00</strong>
                </div>
              </div>

              <div class="field">
                <label for="nome">Nome</label>
                <input id="nome" placeholder="Seu nome" autocomplete="name" />
              </div>

              <div class="field">
                <label for="modo">Entrega ou retirada?</label>
                <select id="modo">
                  <option value="entrega">Entrega</option>
                  <option value="retirada">Retirada</option>
                </select>
              </div>

              <div class="field" id="enderecoBox">
                <label for="endereco">Endereço (para entrega)</label>
                <textarea id="endereco" placeholder="Rua, número, bairro, referência..."></textarea>
              </div>

              <div class="field">
                <label for="pagamento">Forma de pagamento</label>
                <select id="pagamento">
                  <option value="pix">Pix</option>
                  <option value="cartao">Cartão</option>
                  <option value="dinheiro">Dinheiro</option>
                </select>
              </div>

              <div class="field">
                <label for="obs">Observações</label>
                <textarea id="obs" placeholder="Sem cebola, ponto da carne, trocar molho, etc."></textarea>
              </div>

              <div class="cartActions">
                <button class="btnGhost" id="btnLimpar" type="button">
                  <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                    <path d="M3 6h18" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                    <path d="M8 6V4h8v2" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
                    <path d="M7 6l1 16h8l1-16" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
                  </svg>
                  Limpar
                </button>
                <button class="btn" id="btnWhats" type="button">
                  <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                    <path d="M12 21c5 0 9-3.6 9-8s-4-8-9-8-9 3.6-9 8c0 1.6.6 3.1 1.7 4.4L3 21l3.1-1.1C7.7 20.6 9.8 21 12 21Z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/>
                    <path d="M8.4 10.2c.3-.7.6-.8 1.1-.7l.8.2c.3.1.5.4.4.8-.1.5-.1 1 .2 1.5.3.5.8 1.1 1.4 1.5.5.3 1 .4 1.5.2.4-.1.7.1.8.4l.2.8c.1.5 0 .8-.7 1.1-.8.4-1.7.4-2.7 0-1.2-.5-2.4-1.6-3.4-3.4-.4-1-.4-1.9 0-2.7Z" fill="currentColor" opacity=".9"/>
                  </svg>
                  Finalizar no WhatsApp
                </button>
              </div>

              <p class="hint">
                O site monta a mensagem automaticamente. Você só confirma e envia no WhatsApp.
              </p>
            </aside>
          </div>
        </div>
      </div>
    </section>

    <section id="combos">
      <div class="wrap">
        <div class="sectionHead reveal">
          <div class="stack" style="gap:6px">
            <h3>Combos (aumente o ticket)</h3>
            <p>Ofertas prontas para vender mais. Você pode editar os nomes e preços no código.</p>
          </div>
        </div>

        <div class="infoBand">
          <article class="panel reveal d2">
            <h4>Três combos que vendem bem</h4>
            <p>
              Use como sugestão no atendimento. Aqui eles também entram no carrinho com 1 clique.
            </p>
            <div class="bullets" style="margin-top:14px">
              <div class="bullet">
                <b>Combo Brasa</b>
                <span>Burger + batata (P) + refri lata</span>
                <div style="margin-top:10px; display:flex; gap:10px; align-items:center; justify-content:space-between;">
                  <span style="font-family:Fraunces,serif; font-size:18px;">R$ 34,90</span>
                  <button class="addBtn" type="button" data-add="combo-brasa">Adicionar</button>
                </div>
              </div>
              <div class="bullet">
                <b>Combo Rua</b>
                <span>Hot dog + refri lata</span>
                <div style="margin-top:10px; display:flex; gap:10px; align-items:center; justify-content:space-between;">
                  <span style="font-family:Fraunces,serif; font-size:18px;">R$ 19,90</span>
                  <button class="addBtn" type="button" data-add="combo-rua">Adicionar</button>
                </div>
              </div>
              <div class="bullet">
                <b>Combo Duplo</b>
                <span>2 burgers + 2 refri (lata)</span>
                <div style="margin-top:10px; display:flex; gap:10px; align-items:center; justify-content:space-between;">
                  <span style="font-family:Fraunces,serif; font-size:18px;">R$ 59,90</span>
                  <button class="addBtn" type="button" data-add="combo-duplo">Adicionar</button>
                </div>
              </div>
              <div class="bullet">
                <b>Extras (up-sell)</b>
                <span>Cheddar • Bacon • Catupiry • Ovo</span>
                <div style="margin-top:10px; display:flex; gap:10px; align-items:center; justify-content:space-between;">
                  <span style="font-family:Fraunces,serif; font-size:18px;">a partir de R$ 2,50</span>
                  <a class="addBtn" href="#cardapio" style="text-decoration:none;">Ver extras</a>
                </div>
              </div>
            </div>
          </article>

          <aside class="panel reveal d3" id="como-funciona">
            <h4>Como funciona</h4>
            <p>Um fluxo simples e rápido, do jeito que cliente gosta:</p>
            <div class="bullets" style="margin-top:14px">
              <div class="bullet">
                <b>1) Escolha</b>
                <span>Busque e adicione itens no carrinho.</span>
              </div>
              <div class="bullet">
                <b>2) Ajuste</b>
                <span>Selecione entrega/retirada, pagamento e observações.</span>
              </div>
              <div class="bullet">
                <b>3) Envie</b>
                <span>O WhatsApp abre com a mensagem pronta.</span>
              </div>
              <div class="bullet">
                <b>4) Confirme</b>
                <span>Você confirma taxa e tempo pelo WhatsApp.</span>
              </div>
            </div>
            <p class="hint" style="margin-top:12px">
              Se preferir, dá para trocar o WhatsApp por um checkout próprio futuramente.
            </p>
          </aside>
        </div>
      </div>
    </section>

    <section id="contato">
      <div class="wrap">
        <div class="sectionHead reveal">
          <div class="stack" style="gap:6px">
            <h3>Contato</h3>
            <p>Configure seus dados (nome, WhatsApp e horário). Depois, é só publicar.</p>
          </div>
        </div>

        <div class="infoBand">
          <article class="panel reveal d2">
            <h4>Dados da loja</h4>
            <p class="fine" id="dadosLoja">
              WhatsApp: <b id="lojaWhatsText">+55 (00) 00000-0000</b><br/>
              Horário: <b id="lojaHorarioText">Seg–Dom • 18:00–23:30</b><br/>
              Endereço (retirada): <b id="lojaEnderecoText">Rua Exemplo, 123 — Centro</b>
            </p>
            <p class="hint" style="margin-top:10px">
              Clique em “Configurar” no topo (ou no destaque) para editar e salvar no seu navegador.
            </p>
          </article>

          <aside class="panel reveal d3">
            <h4>Boas práticas</h4>
            <p class="fine">
              • Use nomes curtos e descrições claras.<br/>
              • Mantenha 6–10 itens principais e foque nos mais vendidos.<br/>
              • Crie 2–3 combos e empurre extras (bacon/cheddar).<br/>
              • Deixe o WhatsApp correto com DDD (apenas números).
            </p>
            <div class="cartActions" style="margin-top:14px">
              <button class="btnGhost" id="btnCopiarLink" type="button">Copiar link desta seção</button>
              <button class="btn" id="btnAbrirWhats" type="button">Chamar no WhatsApp</button>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <footer>
      <div class="wrap footGrid">
        <div>
          <div class="brand" style="gap:10px">
            <div class="mark" aria-hidden="true" style="width:34px;height:34px;border-radius:12px;"></div>
            <div>
              <h1 style="font-size:16px;margin:0;">Brasa & Rua <small style="font-size:10px;">Site de pedidos</small></h1>
            </div>
          </div>
          <p class="fine" style="margin-top:10px">
            Este é um arquivo único (HTML) com CSS e JS embutidos. Perfeito para hospedar em qualquer lugar.
            Não usa imagens externas.
          </p>
          <p class="fine" style="margin-top:10px">
            © <span id="year"></span> • Todos os direitos reservados.
          </p>
        </div>

        <div class="links" aria-label="Links rápidos">
          <a href="#cardapio">Cardápio</a>
          <a href="#combos">Combos</a>
          <a href="#como-funciona">Como funciona</a>
          <a href="#contato">Contato</a>
        </div>
      </div>
    </footer>
  </main>

  <!-- Modals -->
  <dialog id="dlgConfig" style="border:0; padding:0; border-radius: 22px; width:min(760px, 92vw); background: transparent;">
    <div style="border:1px solid rgba(246,244,239,.14); border-radius: 22px; background: rgba(10,10,12,.82); backdrop-filter: blur(14px); box-shadow: var(--shadow); overflow:hidden;">
      <div style="padding:16px 16px; border-bottom: 1px solid rgba(246,244,239,.10); display:flex; justify-content:space-between; align-items:center; gap:10px;">
        <div>
          <div style="color: rgba(246,244,239,.6); font-weight:900; letter-spacing:.16em; text-transform:uppercase; font-size: 11px;">Configurações</div>
          <div style="font-family:Fraunces,serif; font-size: 22px; letter-spacing:-.02em; margin-top:2px;">Personalize sua loja</div>
        </div>
        <form method="dialog">
          <button class="btnGhost" type="submit" aria-label="Fechar">Fechar</button>
        </form>
      </div>

      <div style="padding:16px; display:grid; grid-template-columns: 1fr 1fr; gap:12px;">
        <div class="field">
          <label for="cfgNomeLoja">Nome da loja</label>
          <input id="cfgNomeLoja" placeholder="Ex.: Brasa & Rua" />
        </div>
        <div class="field">
          <label for="cfgWhats">WhatsApp (somente números)</label>
          <input id="cfgWhats" placeholder="5511999999999" inputmode="numeric" />
        </div>

        <div class="field">
          <label for="cfgHorario">Texto do horário</label>
          <input id="cfgHorario" placeholder="Seg–Dom • 18:00–23:30" />
        </div>
        <div class="field">
          <label for="cfgEndereco">Endereço (retirada)</label>
          <input id="cfgEndereco" placeholder="Rua Exemplo, 123 — Bairro" />
        </div>

        <div class="field" style="grid-column: 1 / -1;">
          <label for="cfgMensagemTopo">Texto do topo (status)</label>
          <input id="cfgMensagemTopo" placeholder="Aberto agora" />
        </div>

        <div class="field" style="grid-column: 1 / -1;">
          <label for="cfgObsLoja">Observação fixa (vai no WhatsApp)</label>
          <textarea id="cfgObsLoja" placeholder="Ex.: Taxa e tempo confirmados após endereço."></textarea>
        </div>
      </div>

      <div style="padding:16px; border-top:1px solid rgba(246,244,239,.10); display:flex; gap:10px; justify-content:flex-end; flex-wrap:wrap;">
        <button class="btnGhost" id="btnResetCfg" type="button">Restaurar padrão</button>
        <button class="btn" id="btnSalvarCfg" type="button">Salvar</button>
      </div>
    </div>
  </dialog>

  <script>
    // -----------------------------
    // Data (edit freely)
    // -----------------------------
    const MENU = [
      {id:"b-smash", cat:"burger", nome:"Smash Clássico", preco:18.90, desc:"Pão brioche, 1 smash 100g, queijo, cebola roxa, picles e molho da casa.", tags:["Mais vendido"], badge:"hot"},
      {id:"b-cheddar-bacon", cat:"burger", nome:"Cheddar & Bacon", preco:24.90, desc:"Pão brioche, burger 160g, cheddar cremoso, bacon crocante e maionese defumada.", tags:["Premium"], badge:"hot"},
      {id:"b-frango", cat:"burger", nome:"Chicken Crocante", preco:21.90, desc:"Frango empanado crocante, alface, tomate e molho levemente picante.", tags:["Crocante"], badge:"hot"},
      {id:"b-veg", cat:"burger", nome:"Veggie Grelhado", preco:22.90, desc:"Hambúrguer vegetal, queijo, rúcula, tomate e molho cítrico.", tags:["Sem carne"], badge:"hot"},

      {id:"b-duplo", cat:"burger", nome:"Duplo Smash", preco:29.90, desc:"Pão brioche, 2 smash 100g, queijo cheddar, bacon e maionese especial.", tags:["Premium", "Mais vendido"], badge:"hot"},
      {id:"b-queijo-azul", cat:"burger", nome:"Blue Cheese Burger", preco:27.50, desc:"Burger 160g, queijo azul, cebola caramelizada e rúcula.", tags:["Especial"], badge:"hot"},

      {id:"h-trad", cat:"hotdog", nome:"Hot Dog Tradicional", preco:14.90, desc:"Salsicha, purê, vinagrete, batata palha e ketchup/mostarda.", tags:["Raiz"], badge:"hot"},
      {id:"h-duplo", cat:"hotdog", nome:"Hot Dog Duplo", preco:18.90, desc:"2 salsichas, purê, cheddar, batata palha e vinagrete.", tags:["Fome grande"], badge:"hot"},
      {id:"h-catupiry", cat:"hotdog", nome:"Hot Dog Catupiry", preco:17.90, desc:"Salsicha, catupiry, milho, batata palha e molho.", tags:["Cremoso"], badge:"hot"},
      {id:"h-bacon", cat:"hotdog", nome:"Hot Dog Bacon", preco:19.90, desc:"Salsicha, bacon, cheddar, batata palha e molho barbecue.", tags:["Forte"], badge:"hot"},
      {id:"h-veggie", cat:"hotdog", nome:"Hot Dog Veggie", preco:18.50, desc:"Salsicha vegetal, alface, tomate e molho especial.", tags:["Sem carne"], badge:"hot"},

      {id:"d-coca", cat:"bebida", nome:"Refrigerante Lata 350ml", preco:6.50, desc:"Coca/Guaraná/Sprite (informe no pedido).", tags:["Gelado"], badge:"ice"},
      {id:"d-agua", cat:"bebida", nome:"Água 500ml", preco:3.50, desc:"Sem gás / com gás (informe no pedido).", tags:["Leve"], badge:"ice"},
      {id:"d-suco", cat:"bebida", nome:"Suco Natural 400ml", preco:9.90, desc:"Laranja / limão / maracujá (informe no pedido).", tags:["Natural"], badge:"ice"},
      {id:"d-cerveja", cat:"bebida", nome:"Cerveja Long Neck 355ml", preco:8.90, desc:"Cerveja gelada para acompanhar seu lanche.", tags:["Gelado"], badge:"ice"},
      {id:"d-energetico", cat:"bebida", nome:"Energético 250ml", preco:9.50, desc:"Para dar aquela energia extra.", tags:["Gelado"], badge:"ice"},

      {id:"x-cheddar", cat:"extra", nome:"Extra Cheddar", preco:3.50, desc:"Porção extra de cheddar cremoso.", tags:["Up-sell"]},
      {id:"x-bacon", cat:"extra", nome:"Extra Bacon", preco:4.50, desc:"Bacon crocante (porção).", tags:["Up-sell"]},
      {id:"x-ovo", cat:"extra", nome:"Extra Ovo", preco:2.50, desc:"1 ovo frito.", tags:["Up-sell"]},
      {id:"x-catupiry", cat:"extra", nome:"Extra Catupiry", preco:3.50, desc:"Porção extra de catupiry.", tags:["Up-sell"]},
      {id:"x-molho-barbecue", cat:"extra", nome:"Extra Molho Barbecue", preco:2.50, desc:"Porção extra de molho barbecue.", tags:["Up-sell"]},
      {id:"x-picles", cat:"extra", nome:"Extra Picles", preco:2.00, desc:"Porção extra de picles crocante.", tags:["Up-sell"]},
    ];

    const COMBOS = {
      "combo-brasa": {id:"combo-brasa", cat:"combo", nome:"Combo Brasa", preco:34.90, desc:"Burger + batata (P) + refri lata", tags:["Combo"], badge:"hot"},
      "combo-rua": {id:"combo-rua", cat:"combo", nome:"Combo Rua", preco:19.90, desc:"Hot dog + refri lata", tags:["Combo"], badge:"hot"},
      "combo-duplo": {id:"combo-duplo", cat:"combo", nome:"Combo Duplo", preco:59.90, desc:"2 burgers + 2 refri (lata)", tags:["Combo"], badge:"hot"}
    };

    // -----------------------------
    // Config (persisted in localStorage)
    // -----------------------------
    const DEFAULT_CFG = {
      nomeLoja: "Brasa & Rua",
      whats: "5500000000000", // troque aqui
      horario: "Seg–Dom • 18:00–23:30",
      endereco: "Rua Exemplo, 123 — Centro",
      statusTopo: "Aberto agora",
      obsLoja: "Taxa e tempo confirmados após envio do endereço."
    };
    const CFG_KEY = "brasa_rua_cfg_v1";

    // Taxa fixa de entrega
    const TAXA_ENTREGA = 7.00;

    function loadCfg(){
      try{
        const raw = localStorage.getItem(CFG_KEY);
        if(!raw) return {...DEFAULT_CFG};
        const parsed = JSON.parse(raw);
        return {...DEFAULT_CFG, ...parsed};
      }catch(e){
        return {...DEFAULT_CFG};
      }
    }
    function saveCfg(cfg){
      localStorage.setItem(CFG_KEY, JSON.stringify(cfg));
    }

    let cfg = loadCfg();

    // -----------------------------
    // Helpers
    // -----------------------------
    const brl = (v)=> v.toLocaleString("pt-BR",{style:"currency", currency:"BRL"});
    const $ = (s, el=document)=> el.querySelector(s);
    const $$ = (s, el=document)=> Array.from(el.querySelectorAll(s));

    function onlyDigits(str){ return (str||"").replace(/\D/g,""); }

    function buildWhatsUrl(phoneDigits, text){
      const phone = onlyDigits(phoneDigits);
      const msg = encodeURIComponent(text);
      return `https://wa.me/${phone}?text=${msg}`;
    }

    // -----------------------------
    // Rendering menu
    // -----------------------------
    const menuList = $("#menuList");
    const q = $("#q");
    const chips = $$(".chip");

    let currentFilter = "todos";

    function groupLabel(cat){
      return ({
        burger:"Hambúrgueres",
        hotdog:"Cachorro-quente",
        bebida:"Bebidas",
        extra:"Extras"
      })[cat] || "Itens";
    }

    function renderMenu(){
      const term = (q.value || "").trim().toLowerCase();
      const items = MENU.filter(it=>{
        const matchTerm = !term || [it.nome,it.desc,(it.tags||[]).join(" ")].join(" ").toLowerCase().includes(term);
        const matchFilter = currentFilter==="todos" ? true : it.cat===currentFilter;
        return matchTerm && matchFilter;
      });

      // Group by category in fixed order
      const order = ["burger","hotdog","bebida","extra"];
      const groups = order.map(cat => ({cat, items: items.filter(i=>i.cat===cat)}))
                          .filter(g=>g.items.length);

      menuList.innerHTML = "";
      if(groups.length === 0){
        menuList.innerHTML = `
          <div style="padding:18px 14px; color: rgba(246,244,239,.7);">
            Nada encontrado. Tente outro termo (ex.: <b>cheddar</b>, <b>hot dog</b>, <b>refri</b>).
          </div>
        `;
        return;
      }

      for(const g of groups){
        const head = document.createElement("div");
        head.className = "menuGroup";
        head.textContent = groupLabel(g.cat);
        menuList.appendChild(head);

        for(const it of g.items){
          const row = document.createElement("div");
          row.className = "item";
          row.setAttribute("data-id", it.id);

          const left = document.createElement("div");
          left.innerHTML = `
            <div class="itemTitle">
              <b>${it.nome}</b>
              <div class="badges">
                ${(it.tags||[]).slice(0,2).map(t=>`<span class="badge ${it.badge||""}">${t}</span>`).join("")}
              </div>
            </div>
            <div class="itemDesc">${it.desc}</div>
          `;

          const right = document.createElement("div");
          right.className = "itemRight";
          right.innerHTML = `
            <div class="itemPrice">${brl(it.preco)}</div>
            <button class="addBtn" type="button" data-add="${it.id}">
              <svg class="icon" viewBox="0 0 24 24" fill="none" aria-hidden="true">
                <path d="M12 5v14M5 12h14" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
              Add
            </button>
          `;

          row.appendChild(left);
          row.appendChild(right);
          menuList.appendChild(row);
        }
      }
    }

    // -----------------------------
    // Cart
    // -----------------------------
    const CART_KEY = "brasa_rua_cart_v1";
    let cart = loadCart();

    function loadCart(){
      try{
        const raw = localStorage.getItem(CART_KEY);
        if(!raw) return {};
        const parsed = JSON.parse(raw);
        return parsed && typeof parsed === "object" ? parsed : {};
      }catch(e){ return {}; }
    }
    function saveCart(){
      localStorage.setItem(CART_KEY, JSON.stringify(cart));
    }

    function findItem(id){
      return MENU.find(i=>i.id===id) || COMBOS[id] || null;
    }

    function addToCart(id){
      const item = findItem(id);
      if(!item) return;
      cart[id] = (cart[id] || 0) + 1;
      saveCart();
      renderCart();
      pulseCartButton();
    }
    function decFromCart(id){
      if(!cart[id]) return;
      cart[id] -= 1;
      if(cart[id] <= 0) delete cart[id];
      saveCart();
      renderCart();
    }
    function incInCart(id){
      if(!cart[id]) cart[id]=0;
      cart[id] += 1;
      saveCart();
      renderCart();
    }
    function clearCart(){
      cart = {};
      saveCart();
      renderCart();
    }

    const cartList = $("#cartList");
    const subtotalEl = $("#subtotal");
    const totalEl = $("#total");
    const entregaEl = $("#entrega");
    const cartCount = $("#cartCount");
    const cartMini = $("#cartMini");

    function cartItemsArray(){
      return Object.entries(cart)
        .map(([id,qty])=>({ item: findItem(id), id, qty }))
        .filter(x=>x.item);
    }

    function calcSubtotal(){
      return cartItemsArray().reduce((acc, x)=> acc + x.item.preco * x.qty, 0);
    }

    function renderCart(){
      const arr = cartItemsArray();
      const count = arr.reduce((a,x)=>a+x.qty,0);

      cartCount.textContent = `(${count})`;
      cartMini.textContent = `${count} ${count===1 ? "item" : "itens"}`;

      if(arr.length === 0){
        cartList.innerHTML = `
          <div style="padding:14px 12px; color: rgba(246,244,239,.72);">
            Seu carrinho está vazio.<br/>
            <span style="color: rgba(246,244,239,.52); font-weight:700;">Adicione um burger, hot dog ou bebida ao lado.</span>
          </div>
        `;
      }else{
        cartList.innerHTML = arr.map(({item,id,qty})=>`
          <div class="cartRow">
            <div>
              <b>${item.nome}</b>
              <small>${item.desc}</small>
              <small style="margin-top:7px; color: rgba(246,244,239,.82); font-weight:800;">
                ${brl(item.preco)} <span style="color: rgba(246,244,239,.52); font-weight:700;">cada</span>
              </small>
            </div>
            <div class="qty" aria-label="Quantidade">
              <button type="button" aria-label="Diminuir" data-dec="${id}">–</button>
              <span aria-label="Quantidade atual">${qty}</span>
              <button type="button" aria-label="Aumentar" data-inc="${id}">+</button>
            </div>
          </div>
        `).join("");
      }

      const subtotal = calcSubtotal();
      subtotalEl.textContent = brl(subtotal);

      // Mostrar taxa fixa se modo for entrega
      const isEntrega = modoEl.value === "entrega";
      entregaEl.textContent = isEntrega ? brl(TAXA_ENTREGA) : "—";

      const total = isEntrega ? subtotal + TAXA_ENTREGA : subtotal;
      totalEl.textContent = brl(total);

      // bind qty buttons
      $$("[data-dec]", cartList).forEach(btn => btn.addEventListener("click", ()=> decFromCart(btn.dataset.dec)));
      $$("[data-inc]", cartList).forEach(btn => btn.addEventListener("click", ()=> incInCart(btn.dataset.inc)));
    }

    function pulseCartButton(){
      const btn = $("#btnVerCarrinho");
      btn.animate([
        { transform:"translateY(0) scale(1)" },
        { transform:"translateY(-2px) scale(1.02)" },
        { transform:"translateY(0) scale(1)" }
      ], { duration: 280, easing:"cubic-bezier(.2,.8,.2,1)" });
    }

    // -----------------------------
    // WhatsApp checkout
    // -----------------------------
    const nomeEl = $("#nome");
    const modoEl = $("#modo");
    const enderecoBox = $("#enderecoBox");
    const enderecoEl = $("#endereco");
    const pagamentoEl = $("#pagamento");
    const obsEl = $("#obs");

    function syncModo(){
      const isEntrega = modoEl.value === "entrega";
      enderecoBox.style.display = isEntrega ? "flex" : "none";
    }

    function buildOrderText(){
      const arr = cartItemsArray();
      const subtotal = calcSubtotal();

      const nome = (nomeEl.value || "").trim();
      const modo = modoEl.value;
      const pagamento = pagamentoEl.value;
      const endereco = (enderecoEl.value || "").trim();
      const obs = (obsEl.value || "").trim();

      const pagLabel = ({pix:"Pix", cartao:"Cartão", dinheiro:"Dinheiro"})[pagamento] || pagamento;

      const lines = [];
      lines.push(`Olá! Quero fazer um pedido na *${cfg.nomeLoja}*.`);
      lines.push("");
      if(nome) lines.push(`*Cliente:* ${nome}`);
      lines.push(`*Modo:* ${modo === "entrega" ? "Entrega" : "Retirada"}`);
      if(modo === "entrega" && endereco) lines.push(`*Endereço:* ${endereco}`);
      lines.push(`*Pagamento:* ${pagLabel}`);
      lines.push("");
      lines.push("*Itens:*");
      for(const {item, qty} of arr){
        lines.push(`• ${qty}x ${item.nome} — ${brl(item.preco * qty)}`);
      }
      lines.push("");
      lines.push(`*Subtotal:* ${brl(subtotal)}`);
      if(modo === "entrega"){
        lines.push(`*Entrega:* ${brl(TAXA_ENTREGA)}`);
      } else {
        lines.push(`*Entrega:* —`);
      }
      lines.push(`*Total:* ${brl(modo === "entrega" ? subtotal + TAXA_ENTREGA : subtotal)}`);
      if(obs) {
        lines.push("");
        lines.push(`*Observações:* ${obs}`);
      }
      if(cfg.obsLoja){
        lines.push("");
        lines.push(`_${cfg.obsLoja}_`);
      }
      return lines.join("\n");
    }

    function checkoutWhats(){
      const arr = cartItemsArray();
      if(arr.length === 0){
        alert("Seu carrinho está vazio. Adicione itens antes de finalizar.");
        return;
      }
      if(modoEl.value === "entrega" && !(enderecoEl.value||"").trim()){
        const ok = confirm("Você escolheu ENTREGA, mas não preencheu o endereço. Deseja continuar mesmo assim?");
        if(!ok) return;
      }
      const text = buildOrderText();
      const url = buildWhatsUrl(cfg.whats, text);
      window.open(url, "_blank", "noopener,noreferrer");
    }

    // -----------------------------
    // Config modal
    // -----------------------------
    const dlg = $("#dlgConfig");
    const cfgNomeLoja = $("#cfgNomeLoja");
    const cfgWhats = $("#cfgWhats");
    const cfgHorario = $("#cfgHorario");
    const cfgEndereco = $("#cfgEndereco");
    const cfgMensagemTopo = $("#cfgMensagemTopo");
    const cfgObsLoja = $("#cfgObsLoja");

    function applyCfgToUI(){
      // Brand title
      document.title = `${cfg.nomeLoja} — Hambúrguer • Hot Dog • Bebidas`;
      $(".brand h1").childNodes[0].textContent = cfg.nomeLoja + " ";
      $("#statusLoja").textContent = cfg.statusTopo;
      $("#horarioTexto").textContent = cfg.horario;
      $("#taxaEntregaTexto").textContent = `R$ ${TAXA_ENTREGA.toFixed(2)} fixa`;

      $("#lojaWhatsText").textContent = formatPhone(cfg.whats);
      $("#lojaHorarioText").textContent = cfg.horario;
      $("#lojaEnderecoText").textContent = cfg.endereco;

      // contact summary
      $("#dadosLoja").innerHTML = `
        WhatsApp: <b id="lojaWhatsText">${formatPhone(cfg.whats)}</b><br/>
        Horário: <b id="lojaHorarioText">${escapeHtml(cfg.horario)}</b><br/>
        Endereço (retirada): <b id="lojaEnderecoText">${escapeHtml(cfg.endereco)}</b>
      `;
    }

    function openCfg(){
      cfgNomeLoja.value = cfg.nomeLoja;
      cfgWhats.value = onlyDigits(cfg.whats);
      cfgHorario.value = cfg.horario;
      cfgEndereco.value = cfg.endereco;
      cfgMensagemTopo.value = cfg.statusTopo;
      cfgObsLoja.value = cfg.obsLoja || "";
      dlg.showModal();
    }

    function saveCfgFromModal(){
      const newCfg = {
        nomeLoja: (cfgNomeLoja.value||"").trim() || DEFAULT_CFG.nomeLoja,
        whats: onlyDigits(cfgWhats.value||"") || DEFAULT_CFG.whats,
        horario: (cfgHorario.value||"").trim() || DEFAULT_CFG.horario,
        endereco: (cfgEndereco.value||"").trim() || DEFAULT_CFG.endereco,
        statusTopo: (cfgMensagemTopo.value||"").trim() || DEFAULT_CFG.statusTopo,
        obsLoja: (cfgObsLoja.value||"").trim()
      };
      cfg = newCfg;
      saveCfg(cfg);
      applyCfgToUI();
      dlg.close();
    }

    function resetCfg(){
      if(!confirm("Restaurar as configurações padrão?")) return;
      cfg = {...DEFAULT_CFG};
      saveCfg(cfg);
      applyCfgToUI();
      openCfg();
    }

    function escapeHtml(str){
      return (str||"").replace(/[&<>"']/g, m => ({
        "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#039;"
      }[m]));
    }

    function formatPhone(digits){
      const d = onlyDigits(digits);
      if(d.length < 10) return "+"+d;
      // basic BR format if possible
      // expected: 55 + DDD(2) + number(8/9)
      if(d.startsWith("55") && d.length >= 12){
        const country = d.slice(0,2);
        const ddd = d.slice(2,4);
        const num = d.slice(4);
        if(num.length === 9) return `+${country} (${ddd}) ${num.slice(0,5)}-${num.slice(5)}`;
        if(num.length === 8) return `+${country} (${ddd}) ${num.slice(0,4)}-${num.slice(4)}`;
      }
      return "+"+d;
    }

    // -----------------------------
    // Scroll reveal (IntersectionObserver)
    // -----------------------------
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          e.target.style.animationPlayState = "running";
          io.unobserve(e.target);
        }
      });
    }, {threshold: .12});

    function setupReveals(){
      $$(".reveal").forEach(el=>{
        el.style.animationPlayState = "paused";
        io.observe(el);
      });
    }

    // -----------------------------
    // Events
    // -----------------------------
    document.addEventListener("click", (ev)=>{
      const add = ev.target.closest("[data-add]");
      if(add) addToCart(add.dataset.add);
    });

    q.addEventListener("input", renderMenu);

    chips.forEach(ch=>{
      ch.addEventListener("click", ()=>{
        chips.forEach(c=>c.setAttribute("aria-pressed","false"));
        ch.setAttribute("aria-pressed","true");
        currentFilter = ch.dataset.filter;
        renderMenu();
      });
    });

    $("#btnWhats").addEventListener("click", checkoutWhats);
    $("#btnLimpar").addEventListener("click", ()=>{
      if(Object.keys(cart).length===0) return;
      if(confirm("Deseja limpar o carrinho?")) clearCart();
    });

    $("#btnVerCarrinho").addEventListener("click", ()=>{
      $("#carrinho").scrollIntoView({behavior:"smooth", block:"start"});
    });

    $("#btnRolagemCombos").addEventListener("click", ()=>{
      $("#combos").scrollIntoView({behavior:"smooth", block:"start"});
    });

    $("#btnPedirDestaque").addEventListener("click", ()=>{
      addToCart("combo-brasa");
      $("#carrinho").scrollIntoView({behavior:"smooth", block:"start"});
    });

    $("#btnConfig").addEventListener("click", openCfg);
    $("#btnSalvarCfg").addEventListener("click", saveCfgFromModal);
    $("#btnResetCfg").addEventListener("click", resetCfg);

    modoEl.addEventListener("change", ()=>{
      syncModo();
      renderCart();
    });

    $("#btnCopiarLink").addEventListener("click", async ()=>{
      const url = location.href.split("#")[0] + "#contato";
      try{
        await navigator.clipboard.writeText(url);
        alert("Link copiado!");
      }catch(e){
        prompt("Copie o link:", url);
      }
    });

    $("#btnAbrirWhats").addEventListener("click", ()=>{
      const url = buildWhatsUrl(cfg.whats, `Olá! Vim pelo site da *${cfg.nomeLoja}* 😄`);
      window.open(url, "_blank", "noopener,noreferrer");
    });

    // -----------------------------
    // Init
    // -----------------------------
    $("#year").textContent = new Date().getFullYear();

    applyCfgToUI();
    renderMenu();
    renderCart();
    syncModo();
    setupReveals();

    // Small UX: allow Esc close dialog (native) + click outside handling
    dlg.addEventListener("click", (e)=>{
      const rect = dlg.getBoundingClientRect();
      const isInDialog =
        e.clientX >= rect.left && e.clientX <= rect.right &&
        e.clientY >= rect.top && e.clientY <= rect.bottom;
      // dialog backdrop click: close when clicking outside the inner panel
      if(e.target === dlg) dlg.close();
    });
  </script>
</body>
</html>
