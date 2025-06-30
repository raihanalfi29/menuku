<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Daftar Menu Makanan</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');
    body {
      background-color: #1a1518;
      font-family: 'Poppins', sans-serif;
      color: #f9f4e7;
      padding: 2rem;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .container {
      max-width: 900px;
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 320px;
      gap: 2.5rem;
      position: relative;
    }
    h1 {
      font-family: 'Fredoka One', cursive;
      font-size: 3.5rem;
      color: #f7c948;
      margin-bottom: 2rem;
      user-select: none;
    }
    .section-title {
      font-family: 'Fredoka One', cursive;
      font-size: 1.5rem;
      color: #f7c948;
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
    }
    .section-title::after {
      content: "";
      flex-grow: 1;
      margin-left: 1rem;
      border-bottom: 2px solid #f7c948;
      max-width: 180px;
      opacity: 0.8;
    }
    ul.menu-list {
      list-style: none;
      padding: 0;
      margin: 0 0 3rem 0;
    }
    ul.menu-list li {
      font-size: 1.1rem;
      line-height: 1.8;
      display: flex;
      justify-content: space-between;
      border-bottom: 2px solid transparent;
      padding: 0.2rem 0;
      gap: 1rem;
      user-select: none;
    }
    ul.menu-list li span.name {
      flex-shrink: 0;
    }
    ul.menu-list li span.dots {
      flex-grow: 1;
      border-bottom: 2px solid #f7c948;
      margin: 0 0.5rem;
      min-width: 50px;
    }
    ul.menu-list li span.price {
      flex-shrink: 0;
      min-width: 60px;
      text-align: right;
      font-variant-numeric: tabular-nums;
    }
    .images-column {
      display: flex;
      flex-direction: column;
      gap: 2rem;
      justify-content: center;
    }
    .image-wrapper {
      border: 4px solid #f9f4e7;
      border-radius: 9999px;
      overflow: hidden;
      width: 280px;
      height: 280px;
      box-shadow: 0 3px 15px rgb(247 201 72 / 0.7);
      background-color: #3a2f38;
      flex-shrink: 0;
    }
    .image-wrapper img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      filter: drop-shadow(0 1px 1px rgb(0 0 0 / 0.3));
      transition: transform 0.4s ease;
    }
    .image-wrapper img:hover {
      transform: scale(1.05);
    }
    .footer-order {
      position: absolute;
      bottom: 0;
      left: 0;
      background-color: #c75710;
      color: #fff9e7;
      padding: 1rem 2rem;
      border-top-right-radius: 32px;
      font-weight: 600;
      font-size: 1.1rem;
      user-select: none;
      letter-spacing: 0.04rem;
      box-shadow: 0 5px 15px rgb(199 87 16 / 0.9);
    }

    /* Decorative lines */
    .decorative-line-1, .decorative-line-2 {
      position: absolute;
      border: 2px solid #f7c94880;
      width: 90px;
      height: 1px;
      top: 128px; /* close to Makanan heading line length */
    }
    .decorative-line-1 {
      left: 218px;
    }
    .decorative-line-2 {
      left: 218px;
      top: 375px;
    }
    /* Small geometric shapes */
    .dot-grid {
      position: absolute;
      width: 30px;
      height: 30px;
      border-radius: 2px;
      box-shadow:
        0px 0px 0 #f7c94888,
        6px 0px 0 #f7c94888,
        12px 0px 0 #f7c94888,
        0px 6px 0 #f7c94888,
        6px 6px 0 #f7c94888,
        12px 6px 0 #f7c94888,
        0px 12px 0 #f7c94888,
        6px 12px 0 #f7c94888,
        12px 12px 0 #f7c94888;
    }
    .dot-top-right {
      top: 2rem;
      right: 2rem;
    }
    .dot-bottom-right {
      bottom: 2rem;
      right: 2rem;
    }
    /* Zigzag lines - decorative */
    .zigzag {
      position: absolute;
      border-bottom: 3px solid #f7c94880;
      width: 55px;
      height: 20px;
      top: 270px;
      left: 20px;
      clip-path: polygon(0% 50%, 10% 100%, 20% 50%, 30% 100%, 40% 50%, 50% 100%, 60% 50%, 70% 100%, 80% 50%, 90% 100%, 100% 50%);
    }
    .zigzag2 {
      top: 190px;
      left: 20px;
    }

    @media (max-width: 720px) {
      body {
        padding: 1rem;
      }
      .container {
        grid-template-columns: 1fr;
      }
      .images-column {
        flex-direction: row;
        justify-content: center;
        gap: 1rem;
        margin-top: 2rem;
      }
      .image-wrapper {
        width: 180px;
        height: 180px;
      }
      h1 {
        font-size: 2.5rem;
        text-align: center;
      }
      .footer-order {
        position: static;
        margin-top: 2rem;
        border-radius: 12px;
        text-align: center;
        box-shadow: none;
      }
      .decorative-line-1,
      .decorative-line-2,
      .dot-grid,
      .zigzag {
        display: none;
      }
    }
  </style>
</head>
<body>
  <main class="container" role="main" aria-label="Daftar Menu Makanan dan Minuman">
    <section>
      <h1 tabindex="0">DAFTAR MENU</h1>

      <h2 class="section-title" tabindex="0">MAKANAN</h2>
      <span class="decorative-line-1" aria-hidden="true"></span>
      <ul class="menu-list" aria-label="Menu Makanan">
        <li><span class="name">Mie Goreng</span><span class="dots" aria-hidden="true"></span><span class="price">12.000</span></li>
        <li><span class="name">Mie Goreng Telur</span><span class="dots" aria-hidden="true"></span><span class="price">15.000</span></li>
        <li><span class="name">Mie Goreng Ayam</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Mie Goreng Seafood</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Mie Goreng Spesial</span><span class="dots" aria-hidden="true"></span><span class="price">22.000</span></li>
      </ul>

      <ul class="menu-list" aria-label="Menu Nasi Goreng">
        <li><span class="name">Nasi Goreng</span><span class="dots" aria-hidden="true"></span><span class="price">12.000</span></li>
        <li><span class="name">Nasi Goreng Telur</span><span class="dots" aria-hidden="true"></span><span class="price">15.000</span></li>
        <li><span class="name">Nasi Goreng Ayam</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Nasi Goreng Seafood</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Nasi Goreng Spesial</span><span class="dots" aria-hidden="true"></span><span class="price">22.000</span></li>
      </ul>

      <ul class="menu-list" aria-label="Menu Kwetiaw Goreng">
        <li><span class="name">Kwetiaw Goreng</span><span class="dots" aria-hidden="true"></span><span class="price">12.000</span></li>
        <li><span class="name">Kwetiaw Goreng Telur</span><span class="dots" aria-hidden="true"></span><span class="price">15.000</span></li>
        <li><span class="name">Kwetiaw Goreng Ayam</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Kwetiaw Goreng Seafood</span><span class="dots" aria-hidden="true"></span><span class="price">18.000</span></li>
        <li><span class="name">Kwetiaw Goreng Spesial</span><span class="dots" aria-hidden="true"></span><span class="price">22.000</span></li>
      </ul>

      <h2 class="section-title" tabindex="0">MINUMAN</h2>
      <span class="decorative-line-2" aria-hidden="true"></span>
      <ul class="menu-list" aria-label="Menu Minuman">
        <li><span class="name">Es Teh Tawar</span><span class="dots" aria-hidden="true"></span><span class="price">3.000</span></li>
        <li><span class="name">Es Teh Manis</span><span class="dots" aria-hidden="true"></span><span class="price">5.000</span></li>
        <li><span class="name">Es Kelapa Muda</span><span class="dots" aria-hidden="true"></span><span class="price">8.000</span></li>
        <li><span class="name">Es Teh Tarik</span><span class="dots" aria-hidden="true"></span><span class="price">8.000</span></li>
        <li><span class="name">Es Jeruk</span><span class="dots" aria-hidden="true"></span><span class="price">8.000</span></li>
      </ul>

      <div class="footer-order" tabindex="0" aria-label="Informasi pemesanan">
        Untuk Pemesanan : +123-456-7890
      </div>

      <div class="dot-grid dot-top-right" aria-hidden="true"></div>
      <div class="dot-grid dot-bottom-right" aria-hidden="true"></div>
      <div class="zigzag" aria-hidden="true"></div>
      <div class="zigzag zigzag2" aria-hidden="true"></div>
    </section>

    <aside class="images-column" aria-hidden="true">
      <div class="image-wrapper" title="Foto sepiring mie goreng dengan irisan tomat dan mentimun">
        <img
          src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ae7b3e04-0c46-4c96-a865-efeaf7fe3ac4.png"
          alt="Sepiring mie goreng berwarna coklat keemasan dengan potongan tomat merah dan irisan mentimun hijau di pinggir piring, di atas piring putih datar"
          onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/eae833e0-0e43-41be-865f-ceac7dc755e2.png';"
        />
      </div>
      <div class="image-wrapper" title="Foto sepiring nasi goreng dengan irisan timun">
        <img
          src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/926fe911-f9d2-4690-8aaa-b9427f538375.png"
          alt="Sepiring nasi goreng berwarna coklat kemerahan dengan potongan sayur dan taburan daun hijau serta irisan timun mengelilingi sisi piring, disajikan di atas piring putih bulat"
          onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3352698f-d219-4660-a61c-e864481d0a24.png';"
        />
      </div>
      <div class="image-wrapper" title="Gelaskopi es teh dengan es batu di dalamnya">
        <img
          src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0a37ba3a-392b-46d2-b283-b4708e819a8c.png"
          alt="Gelaskopi kaca berisi es teh berwarna coklat dengan es batu di dalamnya, terlihat embun pada sisi luar gelas yang transparan"
          onerror="this.onerror=null;this.src='https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/c848797f-f683-4a3d-b4f1-f91d3f1681b3.png';"
        />
      </div>
    </aside>
  </main>
</body>
</html>

