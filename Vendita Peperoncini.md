<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>Vendita Peperoncini - Oli e Polveri</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: #fff8f0;
      color: #272727;
      margin: 0;
      padding: 0;
    }
    header {
      background: #e53935;
      color: #fff;
      padding: 1em 0;
      text-align: center;
      font-size: 2em;
      letter-spacing: 1px;
    }
    .container {
      max-width: 900px;
      margin: 2em auto;
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(160, 0, 0, 0.08);
      padding: 2em;
    }
    h2 {
      color: #e53935;
      margin-top: 1.5em;
    }
    ul {
      list-style: none;
      padding: 0;
    }
    .category {
      margin-bottom: 2em;
    }
    .subcategory li {
      padding: .5em 0;
      border-bottom: 1px solid #eee;
    }
    .subcategory li:last-child {
      border-bottom: none;
    }
    .shop-btn {
      display: inline-block;
      margin-top: 1.5em;
      background: #e53935;
      color: #fff;
      padding: .7em 1.5em;
      border: none;
      border-radius: 5px;
      font-size: 1em;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.25s;
    }
    .shop-btn:hover {
      background: #b71c1c;
    }
    /* Contact Page Styling */
    .contact-page {
      display: none;
    }
    .contact-info {
      font-size: 1.1em;
      margin-top: 1.5em;
    }
    .back-btn {
      margin-top: 2em;
      margin-right: 10px;
      background: #aaa;
      color: #fff;
      padding: .7em 1.2em;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
      font-size: 1em;
      transition: background 0.25s;
      display: inline-block;
    }
    .back-btn:hover { background: #757575; }
    .pay-btn {
      margin-top: 2em;
      background: #25bc1a;
      color: #fff;
      padding: .7em 1.5em;
      border: none;
      border-radius: 5px;
      font-size: 1em;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.25s;
      display: inline-block;
    }
    .pay-btn:hover { background: #0d790b; }
  </style>
  <script>
    function goToContact() {
      document.getElementById('mainpage').style.display = "none";
      document.getElementById('contactpage').style.display = "block";
      window.scrollTo(0,0);
    }
    function goBack() {
      document.getElementById('mainpage').style.display = "block";
      document.getElementById('contactpage').style.display = "none";
      window.scrollTo(0,0);
    }
  </script>
</head>
<body>
  <header>
    Vendita Peperoncini - Oli e Polveri
  </header>
  <main class="container">
    <!-- Pagina principale -->
    <div id="mainpage">
      <section class="category">
        <h2>Olio</h2>
        <ul class="subcategory">
          <li>Olio di Naga Morich Red</li>
          <li>Olio di Black Phanter Striato</li>
          <li>Olio di Habanero Red Savina</li>
          <li>Olio di Apocalypse Chocolate</li>
          <li>Olio di Habanero Chocolate</li>
          <li>Olio di Death Spiral Red</li>
          <li>Olio di Big Mama Black</li>
          <li>Olio di Carolina Reaper Red</li>
          <li>Olio di Scorpion Chocolate</li>
          <li>Olio di Carolina Reaper Chocolate</li>
          <li>Olio di Kraken Peach</li>
        </ul>
        <a class="shop-btn" href="#" onclick="goToContact()">Contattami & Pagamento</a>
      </section>

      <section class="category">
        <h2>Polveri</h2>
        <ul class="subcategory">
          <li>Polvere di Borg 9 Red</li>
          <li>Polvere di Borg 9 Chocolate</li>
          <li>Polvere di Habanero Chocolate</li>
          <li>Polvere di Bhut x Neyde Black Orange</li>
          <li>Polvere di Habanero White</li>
          <li>Polvere di Scotch Bonnet</li>
          <li>Polvere di Naga Morich Red</li>
          <li>Polvere di Carolina Red</li>
          <li>Polvere di Carolina Yellow</li>
          <li>Polvere di Big Mama Mustard</li>
          <li>Polvere di Habanero Caramel</li>
        </ul>
        <a class="shop-btn" href="#" onclick="goToContact()">Contattami & Pagamento</a>
      </section>
    </div>
    <!-- Pagina contatto/pagamento -->
    <div id="contactpage" class="contact-page">
      <h2>Contatti & Pagamento</h2>
      <div class="contact-info">
        <p>
          Per informazioni, ordini o richieste personalizzate contattami su:
          <br><br>
          <strong>Email:</strong> <a href="mailto:salvatore.esempio@email.com">salvatore.esempio@email.com</a>
          <br>
          <strong>Telefono / WhatsApp:</strong> <a href="tel:+393331234567">+39 333 1234567</a>
        </p>
        <p>
          Per effettuare il pagamento, clicca qui:
        </p>
        <a class="pay-btn" href="https://revolut.me/salvatoreepanaai?currency=EUR&amount=1000" target="_blank">Pagamento</a>
      </div>
      <button class="back-btn" onclick="goBack()">Torna alla pagina principale</button>
    </div>
  </main>
</body>
</html>
