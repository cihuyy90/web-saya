# website saya
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Landing Page</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      min-height: 100vh;
      font-family: Arial, sans-serif;
      color: #fff;
      background:
        radial-gradient(circle at 50% 20%, #66343d 0%, transparent 35%),
        linear-gradient(180deg, #45242b 0%, #26151a 100%);
      overflow-x: hidden;
    }

    /* Background titik */
    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      opacity: .35;

      background-image:
        radial-gradient(circle, #b66b78 1.5px, transparent 1.5px);

      background-size: 100px 100px;
    }

    .container {
      width: min(92%, 750px);
      margin: auto;
      padding: 55px 0 80px;
      position: relative;
      z-index: 1;
    }

    /* HEADER */
    .logo {
      text-align: center;
      font-family: Georgia, serif;
      font-size: clamp(38px, 8vw, 58px);
      letter-spacing: 5px;
      color: #eadde0;
      margin-bottom: 28px;
    }

    .description {
      text-align: center;
      color: #cdbbc0;
      font-size: 18px;
      line-height: 1.75;
      letter-spacing: 7px;
      max-width: 680px;
      margin: auto;
    }

    .line {
      height: 1px;
      background: rgba(220, 140, 155, .45);
      margin: 22px 0 62px;
    }

    /* KOTAK BESAR */
    .hero-box {
      height: 740px;
      border: 2px solid rgba(224, 105, 142, .65);
      border-radius: 28px;

      background:
        radial-gradient(circle at 10% 10%, rgba(255,255,255,.04), transparent 30%),
        rgba(35, 20, 25, .45);

      box-shadow:
        0 0 18px rgba(224, 80, 130, .22),
        inset 0 0 30px rgba(0,0,0,.12);

      margin-bottom: 60px;
    }

    /* BUTTON CARD */
    .action {
      display: flex;
      align-items: center;
      gap: 25px;

      min-height: 120px;
      margin-bottom: 30px;
      padding: 16px 18px 16px 35px;

      border: 2px solid #9c49ff;
      border-radius: 25px;

      background: rgba(30, 17, 24, .75);

      box-shadow:
        0 0 10px rgba(150, 55, 255, .18),
        inset 0 0 20px rgba(0,0,0,.15);

      transition: .25s ease;
    }

    .action:hover {
      transform: translateY(-3px);
      box-shadow:
        0 0 22px rgba(180, 70, 255, .4),
        inset 0 0 20px rgba(0,0,0,.2);
    }

    /* ICON */
    .icon {
      width: 70px;
      height: 70px;
      flex-shrink: 0;

      border-radius: 50%;
      border: 2px solid #ffd900;

      display: flex;
      align-items: center;
      justify-content: center;

      background: #171116;

      box-shadow:
        0 0 12px rgba(255, 220, 0, .65),
        inset 0 0 15px rgba(255, 220, 0, .15);
    }

    .icon span {
      width: 35px;
      height: 25px;
      border-radius: 5px;
      background: linear-gradient(
        135deg,
        #8c6a70,
        #f4d44e,
        #8b394d
      );
      display: block;
    }

    .text {
      flex: 1;
    }

    .text h2 {
      font-family: Georgia, serif;
      font-size: 29px;
      letter-spacing: 3px;
      margin-bottom: 8px;
      color: #eee5e7;
    }

    .text p {
      font-size: 17px;
      color: #bdaeb2;
    }

    /* BUTTON */
    .btn {
      width: 235px;
      height: 88px;

      border-radius: 18px;
      border: 2px solid #b765ff;

      background: linear-gradient(
        135deg,
        #24141d,
        #633a4d
      );

      color: white;
      font-size: 23px;
      font-weight: bold;

      cursor: pointer;

      transition: .25s ease;
    }

    .btn:hover {
      transform: scale(1.03);
      box-shadow: 0 0 20px rgba(190, 90, 255, .45);
    }

    /* BUTTON TERANG */
    .btn.light {
      color: #30113f;

      background:
        linear-gradient(
          135deg,
          #fff,
          #e8d9ff
        );

      border-color: #c576ff;

      box-shadow:
        0 0 15px rgba(218, 160, 255, .35);
    }

    /* RESPONSIVE HP */
    @media (max-width: 600px) {

      .container {
        width: 90%;
        padding-top: 45px;
      }

      .description {
        font-size: 13px;
        letter-spacing: 5px;
        line-height: 1.8;
      }

      .hero-box {
        height: 500px;
        border-radius: 22px;
      }

      .action {
        min-height: 105px;
        gap: 14px;
        padding: 12px;
      }

      .icon {
        width: 55px;
        height: 55px;
      }

      .icon span {
        width: 28px;
        height: 20px;
      }

      .text h2 {
        font-size: 20px;
        letter-spacing: 2px;
      }

      .text p {
        font-size: 12px;
      }

      .btn {
        width: 110px;
        height: 65px;
        font-size: 17px;
      }
    }
  </style>
</head>

<body>

  <main class="container">

    <h1 class="logo">MY WEBSITE</h1>

    <p class="description">
      PLATFORM DIGITAL DENGAN TAMPILAN MODERN,
      RESPONSIF, DAN MUDAH DIGUNAKAN
    </p>

    <div class="line"></div>

    <!-- AREA UTAMA -->
    <div class="hero-box"></div>

    <!-- ACTION 1 -->
    <div class="action">

      <div class="icon">
        <span></span>
      </div>

      <div class="text">
        <h2>MASUK</h2>
        <p>AKSES AKUN ANDA</p>
      </div>

      <button class="btn" onclick="showMessage('Tombol masuk diklik')">
        MASUK
      </button>

    </div>

    <!-- ACTION 2 -->
    <div class="action">

      <div class="icon">
        <span></span>
      </div>

      <div class="text">
        <h2>DAFTAR</h2>
        <p>BUAT AKUN BARU</p>
      </div>

      <button class="btn" onclick="showMessage('Tombol daftar diklik')">
        DAFTAR
      </button>

    </div>

    <!-- ACTION 3 -->
    <div class="action">

      <div class="icon">
        <span></span>
      </div>

      <div class="text">
        <h2>INFO</h2>
        <p>LIHAT INFORMASI</p>
      </div>

      <button
        class="btn light"
        onclick="showMessage('Informasi dibuka')">
        LIHAT
      </button>

    </div>

  </main>

  <script>
    function showMessage(message) {
      alert(message);
    }
  </script>

</body>
</html>