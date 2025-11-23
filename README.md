
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>Peperoncini Premium | Oli & Polveri</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
  <style>
    :root {
      --primary: #d32f2f;
      --primary-dark: #b71c1c;
      --accent: #ff5722;
      --bg-color: #f8f9fa;
      --card-bg: #ffffff;
      --text-main: #2c3e50;
      --text-light: #636e72;
      --shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.08);
    }
    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg-color);
      background-image: radial-gradient(circle at top center, #ffebee 0%, transparent 70%);
      color: var(--text-main);
      margin: 0;
      padding: 0;
      min-height: 100vh;
    }
    header {
      background: transparent;
      padding: 2.5em 1em 1em 1em;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-weight: 800;
      font-size: 2.2em;
      background: linear-gradient(45deg, var(--primary), var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: -1px;
    }
    header p {
      color: var(--text-light);
      font-size: 1em;
      margin-top: 0.5em;
      font-weight: 400;
    }
    .container {
      max-width: 600px;
      margin: 1em auto 4em auto;
      background: var(--card-bg);
      border-radius: 24px;
      box-shadow: var(--shadow);
      padding: 2.5em;
      position: relative;
      overflow: hidden;
    }
    .category-header {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 1em;
      margin-top: 2em;
    }
    .category-header:first-of-type { margin-top: 0; }
    .category-header h2 {
      font-size: 1.4em;
      font-weight: 700;
      color: var(--text-main);
      margin: 0;
    }
    .category-header i {
      color: var(--primary);
      background: #ffebee;
      padding: 8px;
      border-radius: 50%;
      font-size: 0.9em;
    }
    .product-list {
      list-style: none;
      padding: 0;
      margin: 0 0 1.5em 0;
      border: 1px solid #eee;
      border-radius: 16px;
      overflow: hidden;
    }
    .product-list li {
      padding: 0.8em 1.2em;
      border-bottom: 1px solid #f0f0f0;
      font-size: 0.95em;
      color: var(--text-light);
      display: flex;
      align-items: center;
      gap: 8px;
      background: #fff;
      transition: background 0.2s;
      cursor:pointer;
    }
    .product-list li:last-child { border-bottom: none; }
    .product-list li:hover {
      background: #fdfdfd;
      color: var(--primary);
    }
    .product-list li i {
      font-size: 0.8em;
      color: #e0e0e0;
    }
    .btn-primary {
      display: block;
      width: 100%;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      color: white;
      border: none;
      padding: 1em;
      border-radius: 12px;
      font-size: 1em;
      font-weight: 600;
      cursor: pointer;
      text-align: center;
      text-decoration: none;
      transition: transform 0.2s, box-shadow 0.2s;
      box-shadow: 0 4px 15px rgba(211, 47, 47, 0.2);
    }
    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(211, 47, 47, 0.3);
    }
    .btn-primary:disabled {
      opacity: 0.7;
      cursor: not-allowed;
    }
    .btn-outline {
      display: block;
      width: 100%;
      background: transparent;
      color: var(--text-main);
      border: 2px solid #eee;
      padding: 0.9em;
      border-radius: 12px;
      font-size: 0.95em;
      font-weight: 600;
      cursor: pointer;
      text-align: center;
      margin-top: 1em;
      transition: all 0.2s;
    }
    .btn-outline:hover {
      border-color: var(--text-main);
      background: #fff;
    }
    .form-page {
      display: none;
      animation: slideUp 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    }
    @keyframes slideUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .form-label {
      display: block;
      font-size: 0.85em;
      font-weight: 600;
      color: var(--text-main);
      margin-bottom: 0.5em;
      margin-top: 1.2em;
    }
    .form-input, .form-select {
      width: 100%;
      padding: 0.9em;
      border: 1px solid #e0e0e0;
      border-radius: 10px;
      font-family: 'Inter', sans-serif;
      font-size: 1em;
      color: var(--text-main);
      background: #fafafa;
      box-sizing: border-box;
      transition: border-color 0.2s, background 0.2s;
    }
    .form-input:focus, .form-select:focus {
      outline: none;
      border-color: var(--primary);
      background: #fff;
    }
    .footer-contacts {
      text-align: center;
      margin-top: 3em;
      padding-top: 2em;
      border-top: 1px solid #eee;
    }
    .contact-toggle {
      background: none;
      border: none;
      color: var(--text-light);
      font-size: 0.9em;
      cursor: pointer;
      text-decoration: underline;
    }
    .contact-box {
      display: none;
      margin-top: 1em;
      background: #f1f3f5;
      padding: 1em;
      border-radius: 12px;
      font-size: 0.9em;
    }
    .spicy-level {
      letter-spacing: 2px;
      font-size: 1.4em;
      margin-bottom: 0.2em;
      line-height: 1em;
    }
    @media (max-width: 600px) {
      .container {
        margin: 0;
        border-radius: 0;
        box-shadow: none;
        padding: 1.5em;
      }
      body { background: white; }
      header { padding-top: 2em; }
    }
  </style>
  <script>
    function showForm(tipo) {
      hideAll();
      document.getElementById('formOlio').style.display = tipo === "olio" ? "block" : "none";
      document.getElementById('formPolveri').style.display = tipo === "polveri" ? "block" : "none";
      window.scrollTo(0,0);
    }
    function goBack() {
      document.getElementById('mainpage').style.display = "block";
      document.getElementById('formOlio').style.display = "none";
      document.getElementById('formPolveri').style.display = "none";
      hideAllDetails();
      window.scrollTo(0,0);
    }
    function toggleContatti() {
      var box = document.getElementById('contactBox');
      box.style.display = box.style.display === "block" ? "none" : "block";
    }
    function handleFormSubmit(event) {
      event.preventDefault();
      var form = event.target;
      var data = new FormData(form);
      var button = form.querySelector("button[type='submit']");
      var originalText = button.innerHTML;
      button.innerHTML = '<i class="fa-solid fa-circle-notch fa-spin"></i> Elaborazione...';
      button.disabled = true;
      button.style.opacity = "0.8";
      fetch("https://formspree.io/f/movbbypn", {
        method: "POST",
        body: data,
        headers: { 'Accept': 'application/json' }
      })
      .then(() => window.location.href = "https://revolut.me/pangiu?currency=EUR&amount=1000")
      .catch(() => {
        alert("Errore di connessione. Verrai reindirizzato comunque al pagamento.");
        window.location.href = "https://revolut.me/pangiu?currency=EUR&amount=1000";
      });
    }
    function showProductDetail(productId) {
      hideAll();
      document.getElementById('detail_' + productId).style.display = "block";
      window.scrollTo(0,0);
    }
    function hideAll() {
      document.getElementById('mainpage').style.display = "none";
      document.getElementById('formOlio').style.display = "none";
      document.getElementById('formPolveri').style.display = "none";
      hideAllDetails();
    }
    function hideAllDetails() {
      var details = document.querySelectorAll('.detail-page');
      details.forEach(function(el) { el.style.display = "none"; });
    }
  </script>
</head>
<body>
  <header>
    <h1>Peperoncini Premium</h1>
    <p>Oli artigianali & Polveri extra piccanti</p>
  </header>
  <main class="container">
    <div id="mainpage">
      <!-- Sezione Olii -->
      <div class="category-header">
        <i class="fa-solid fa-droplet"></i>
        <h2>Oli Piccanti</h2>
      </div>
      <ul class="product-list">
        <li onclick="showProductDetail('olio_naga')"><i class="fa-solid fa-pepper-hot"></i> Naga Morich Red</li>
        <li onclick="showProductDetail('olio_black')"><i class="fa-solid fa-pepper-hot"></i> Black Phanter Striato</li>
        <li onclick="showProductDetail('olio_habRS')"><i class="fa-solid fa-pepper-hot"></i> Habanero Red Savina</li>
        <li onclick="showProductDetail('olio_apoc')"><i class="fa-solid fa-pepper-hot"></i> Apocalypse Chocolate</li>
        <li onclick="showProductDetail('olio_habChoc')"><i class="fa-solid fa-pepper-hot"></i> Habanero Chocolate</li>
        <li onclick="showProductDetail('olio_death')"><i class="fa-solid fa-pepper-hot"></i> Death Spiral Red</li>
        <li onclick="showProductDetail('olio_bigmama')"><i class="fa-solid fa-pepper-hot"></i> Big Mama Black</li>
        <li onclick="showProductDetail('olio_reaper_red')"><i class="fa-solid fa-pepper-hot"></i> Carolina Reaper Red</li>
        <li onclick="showProductDetail('olio_scorpion')"><i class="fa-solid fa-pepper-hot"></i> Scorpion Chocolate</li>
        <li onclick="showProductDetail('olio_reaper_choc')"><i class="fa-solid fa-pepper-hot"></i> Carolina Reaper Chocolate</li>
        <li onclick="showProductDetail('olio_kraken')"><i class="fa-solid fa-pepper-hot"></i> Kraken Peach</li>
      </ul>
      <button class="btn-primary" onclick="showForm('olio')">Acquista Olio</button>
      <div class="category-header">
        <i class="fa-solid fa-fire"></i>
        <h2>Polveri Extra</h2>
      </div>
      <ul class="product-list">
        <li onclick="showProductDetail('polveri_borgred')"><i class="fa-solid fa-pepper-hot"></i> Borg 9 Red</li>
        <li onclick="showProductDetail('polveri_borgchoc')"><i class="fa-solid fa-pepper-hot"></i> Borg 9 Chocolate</li>
        <li onclick="showProductDetail('polveri_habChoc')"><i class="fa-solid fa-pepper-hot"></i> Habanero Chocolate</li>
        <li onclick="showProductDetail('polveri_bhutneyde')"><i class="fa-solid fa-pepper-hot"></i> Bhut x Neyde Black Orange</li>
        <li onclick="showProductDetail('polveri_habWhite')"><i class="fa-solid fa-pepper-hot"></i> Habanero White</li>
        <li onclick="showProductDetail('polveri_scotch')"><i class="fa-solid fa-pepper-hot"></i> Scotch Bonnet</li>
        <li onclick="showProductDetail('polveri_naga')"><i class="fa-solid fa-pepper-hot"></i> Naga Morich Red</li>
        <li onclick="showProductDetail('polveri_carored')"><i class="fa-solid fa-pepper-hot"></i> Carolina Red</li>
        <li onclick="showProductDetail('polveri_caroyellow')"><i class="fa-solid fa-pepper-hot"></i> Carolina Yellow</li>
        <li onclick="showProductDetail('polveri_bigmama')"><i class="fa-solid fa-pepper-hot"></i> Big Mama Mustard</li>
        <li onclick="showProductDetail('polveri_habCaramel')"><i class="fa-solid fa-pepper-hot"></i> Habanero Caramel</li>
      </ul>
      <button class="btn-primary" onclick="showForm('polveri')">Acquista Polveri</button>
      <!-- SEZIONE CONTATTI -->
      <div class="footer-contacts">
        <button class="contact-toggle" onclick="toggleContatti()">Hai bisogno di aiuto? Contattami</button>
        <div id="contactBox" class="contact-box">
          <p><strong><i class="fa-brands fa-telegram"></i> Telegram:</strong> @peperonciniartigianali</p>
          <p>
            <strong><i class="fa-brands fa-instagram"></i> Instagram:</strong>
            <a href="https://www.instagram.com/peperonciniartigianali.it?igsh=cGJvOWxheDFjaGEz" target="_blank" style="color:inherit; text-decoration:underline;">@peperonciniartigianali.it</a>
          </p>
        </div>
      </div>
    </div>
    <!-- FORM OLIO -->
    <div id="formOlio" class="form-page">
      <div class="category-header">
        <i class="fa-solid fa-cart-shopping"></i>
        <h2>Ordine Olio</h2>
      </div>
      <form onsubmit="handleFormSubmit(event)">
        <label class="form-label">Prodotto</label>
        <select class="form-select" name="prodotto_olio" required>
          <option value="">Seleziona la varietà...</option>
          <option>Olio di Naga Morich Red</option>
          <option>Olio di Black Phanter Striato</option>
          <option>Olio di Habanero Red Savina</option>
          <option>Olio di Apocalypse Chocolate</option>
          <option>Olio di Habanero Chocolate</option>
          <option>Olio di Death Spiral Red</option>
          <option>Olio di Big Mama Black</option>
          <option>Olio di Carolina Reaper Red</option>
          <option>Olio di Scorpion Chocolate</option>
          <option>Olio di Carolina Reaper Chocolate</option>
          <option>Olio di Kraken Peach</option>
        </select>
        <label class="form-label">Indirizzo di Spedizione</label>
        <input type="text" class="form-input" name="stato" placeholder="Stato (es. Italia)" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="citta" placeholder="Città" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="provincia" placeholder="Provincia" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="cap" placeholder="CAP" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="indirizzo" placeholder="Via e Numero Civico" required>
        <div style="margin-top: 2em;">
          <button type="submit" class="btn-primary">
            Vai al Pagamento <i class="fa-solid fa-arrow-right" style="margin-left:5px"></i>
          </button>
          <button type="button" class="btn-outline" onclick="goBack()">Annulla</button>
        </div>
      </form>
    </div>
    <!-- FORM POLVERI -->
    <div id="formPolveri" class="form-page">
      <div class="category-header">
        <i class="fa-solid fa-cart-shopping"></i>
        <h2>Ordine Polveri</h2>
      </div>
      <form onsubmit="handleFormSubmit(event)">
        <label class="form-label">Prodotto</label>
        <select class="form-select" name="prodotto_polveri" required>
          <option value="">Seleziona la varietà...</option>
          <option>Polvere di Borg 9 Red</option>
          <option>Polvere di Borg 9 Chocolate</option>
          <option>Polvere di Habanero Chocolate</option>
          <option>Polvere di Bhut x Neyde Black Orange</option>
          <option>Polvere di Habanero White</option>
          <option>Polvere di Scotch Bonnet</option>
          <option>Polvere di Naga Morich Red</option>
          <option>Polvere di Carolina Red</option>
          <option>Polvere di Carolina Yellow</option>
          <option>Polvere di Big Mama Mustard</option>
          <option>Polvere di Habanero Caramel</option>
        </select>
        <label class="form-label">Indirizzo di Spedizione</label>
        <input type="text" class="form-input" name="stato" placeholder="Stato (es. Italia)" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="citta" placeholder="Città" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="provincia" placeholder="Provincia" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="cap" placeholder="CAP" required style="margin-bottom: 10px;">
        <input type="text" class="form-input" name="indirizzo" placeholder="Via e Numero Civico" required>
        <div style="margin-top: 2em;">
          <button type="submit" class="btn-primary">
            Vai al Pagamento <i class="fa-solid fa-arrow-right" style="margin-left:5px"></i>
          </button>
          <button type="button" class="btn-outline" onclick="goBack()">Annulla</button>
        </div>
      </form>
    </div>
    <!-- PAGINE DETTAGLIO PRODOTTI (undici olio + undici polveri, tutte!) -->
    <div id="detail_olio_naga" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Naga Morich Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> ~800.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Origine India-Bangladesh, profumo fruttato, sapore ricco, note di albicocca.</p>
      <p><b>Prodotto:</b> Olio extravergine con Naga Morich Red a km zero, piccantezza intensa e persistente.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_black" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Black Phanter Striato</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> ~1.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Fruttato, retrogusto affumicato, piccantezza alta, per intenditori.</p>
      <p><b>Prodotto:</b> Olio aromatizzato a km zero, sapore deciso per ricette creative.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_habRS" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Habanero Red Savina</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 350.000–577.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Aroma esotico, tono dolce e pungente, ex record di piccantezza.</p>
      <p><b>Prodotto:</b> Olio caldo, elegante, solo Habanero Red Savina locale, ottimo per salse e marinature.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_apoc" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Apocalypse Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.500.000–2.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Peperoncino italiano super hot, aroma intenso, bruciore potente.</p>
      <p><b>Prodotto:</b> Olio potentissimo, solo per amanti del fuoco, ingredienti a km zero.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_habChoc" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Habanero Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 200.000–425.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Aroma fruttato e cioccolatoso, origine Giamaica.</p>
      <p><b>Prodotto:</b> Olio dal gusto esotico, da Habanero Chocolate a km zero. Perfetto per piatti etnici.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_death" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Death Spiral Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.200.000–1.300.000+ SHU</div>
      <p><b>Descrizione peperoncino:</b> Aroma fruttato/agrumato, bruciore intenso e immediato.</p>
      <p><b>Prodotto:</b> Olio fortissimo, solo peperoncini locali selezionati. Per salse ultra-piccanti.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_bigmama" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Big Mama Black</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.500.000–2.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Frutto grande, colore cioccolato scuro, aroma affumicato e intenso.</p>
      <p><b>Prodotto:</b> Olio aromatico, potentissimo, solo da Big Mama Black locale.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_reaper_red" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Carolina Reaper Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.600.000–2.200.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Il più piccante del mondo, aroma fruttato, bruciore estremo.</p>
      <p><b>Prodotto:</b> Olio esclusivo da Carolina Reaper Red locale, solo per temerari.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_scorpion" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Scorpion Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.200.000–2.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Sapore intenso e aromatico, colore marrone scuro, bruciore forte e prolungato.</p>
      <p><b>Prodotto:</b> Olio super hot, ingredienti locali selezionati, perfetto per chi cerca il massimo.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_reaper_choc" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Carolina Reaper Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.400.000–2.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Variante "cioccolato" della Reaper, sapore ancora più aromatico e forte.</p>
      <p><b>Prodotto:</b> Olio da Carolina Reaper Chocolate locale, per chi vuole il fuoco assoluto.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_olio_kraken" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Olio di Kraken Peach</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> 700.000–900.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Raro, color pesca, sapore fruttato, piccante ma meno estremo.</p>
      <p><b>Prodotto:</b> Olio originale, ingredienti km zero, per chi vuole una piccantezza avvolgente.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <!-- POLVERI (tutte!) -->
    <div id="detail_polveri_borgred" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Borg 9 Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.000.000–1.200.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Incrocio 7 Pot, aromi intensi, bruciore devastante.</p>
      <p><b>Prodotto:</b> Polvere da peperoncini freschi a km zero, ideale per salse, grigliate, primi piatti.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_borgchoc" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Borg 9 Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.100.000–1.300.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Gusto ricco, terroso, forte e persistente.</p>
      <p><b>Prodotto:</b> Polvere da Borg 9 Chocolate a km zero, per veri intenditori del piccante.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_habChoc" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Habanero Chocolate</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 200.000–425.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Aroma fruttato, sapore cioccolatoso.</p>
      <p><b>Prodotto:</b> Polvere gourmet da peperoncini locali, perfetta per piatti etnici e fusion.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_bhutneyde" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Bhut x Neyde Black Orange</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> 750.000–1.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Incrocio raro, profumo agrumato e intenso.</p>
      <p><b>Prodotto:</b> Polvere intensa da peperoncini artigianali a km zero. Perfetta su piatti orientali.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_habWhite" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Habanero White</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 100.000–350.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Peperoncino bianco, fresco e fruttato.</p>
      <p><b>Prodotto:</b> Polvere elegante per chi vuole un tocco di piccante senza esagerare. Solo a km zero.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_scotch" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Scotch Bonnet</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 100.000–350.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Caraibico, aroma fruttato, perfetto per cucine etniche.</p>
      <p><b>Prodotto:</b> Polvere artigianale da filiera corta per sapidità unica e piccantezza tropicale.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_naga" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Naga Morich Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> ~800.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Origine India/Bangladesh, gusto intenso.</p>
      <p><b>Prodotto:</b> Polvere da Naga Morich Red a km zero, perfetta per esplosioni di sapore.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_carored" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Carolina Red</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.600.000–2.200.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Variante Carolina, piccantezza estrema.</p>
      <p><b>Prodotto:</b> Polvere massima, solo da peperoncini locali selezionati.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_caroyellow" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Carolina Yellow</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️🌶️</span> 5 su 5</div>
      <div><b>Scala Scoville:</b> 1.500.000–2.000.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Variante gialla, punta aromatica più fresca.</p>
      <p><b>Prodotto:</b> Polvere potentissima a km zero, perfetta per rendere ogni piatto “di fuoco”.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_bigmama" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Big Mama Mustard</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️</span> 4 su 5</div>
      <div><b>Scala Scoville:</b> 900.000–1.200.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Piccantezza notevole, gusto erbaceo e originale.</p>
      <p><b>Prodotto:</b> Polvere da Big Mama locale, per ricette innovative e creative.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
    <div id="detail_polveri_habCaramel" class="form-page detail-page">
      <div class="category-header"><i class="fa-solid fa-pepper-hot"></i><h2>Polvere di Habanero Caramel</h2></div>
      <div class="spicy-level"><span style="color:#d32f2f;">🌶️🌶️🌶️</span><span style="color:#e0e0e0;">🌶️🌶️</span> 3 su 5</div>
      <div><b>Scala Scoville:</b> 200.000–300.000 SHU</div>
      <p><b>Descrizione peperoncino:</b> Aroma dolce, colore caramello, delicato rispetto ai super-hot.</p>
      <p><b>Prodotto:</b> Polvere gourmet, perfetta per piatti dolci-salati a base di ingredienti locali.</p>
      <button class="btn-outline" onclick="goBack()">Torna indietro</button>
    </div>
  </main>
</body>
</html>

