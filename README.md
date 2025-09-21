<!DOCTYPE html>
<html lang="bg">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Моят магазин за дрехи</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #fafafa;
    }
    header {
      background: #333;
      color: #fff;
      text-align: center;
      padding: 1rem;
    }
    .filters {
      text-align: center;
      margin: 1rem;
    }
    .filters button {
      margin: 0.3rem;
      padding: 0.5rem 1rem;
      border: none;
      background: #555;
      color: #fff;
      cursor: pointer;
      border-radius: 5px;
    }
    .filters button:hover {
      background: #000;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
      padding: 1rem;
    }
    .card {
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      overflow: hidden;
      display: flex;
      flex-direction: column;
    }
    .card img {
      width: 100%;
      height: 250px;
      object-fit: cover;
    }
    .card-content {
      padding: 1rem;
      flex-grow: 1;
    }
    .card h3 {
      margin: 0 0 0.5rem;
    }
    .card p {
      margin: 0.3rem 0;
      font-size: 0.9rem;
    }
    .contact {
      margin-top: 0.5rem;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Моят магазин за дрехи</h1>
  </header>

  <div class="filters">
    <button onclick="filterSize('all')">Всички</button>
    <button onclick="filterSize('XL')">XL</button>
    <button onclick="filterSize('2XL')">2XL</button>
    <button onclick="filterSize('3XL')">3XL</button>
    <button onclick="filterSize('4XL')">4XL</button>
    <button onclick="filterSize('5XL')">5XL</button>
  </div>

  <div class="container">
    <div class="card" data-size="3XL">
      <img src="images/pantalon.jpg" alt="Летен панталон">
      <div class="card-content">
        <h3>Дамски летен панталон</h3>
        <p>Размер: 3XL – БГ №52–54</p>
        <p>Талия 96 см | Ханш 120 см | Дължина 106 см</p>
        <p>Много удобен, тънък и мек панталон в перфектно състояние.</p>
        <div class="contact">📞 WhatsApp/Viber, телефон</div>
      </div>
    </div>

    <div class="card" data-size="4XL">
      <img src="images/riza.jpg" alt="Риза с дантела">
      <div class="card-content">
        <h3>Бяла риза с дантела</h3>
        <p>Размер: 4XL – БГ №54</p>
        <p>Гръдна 130 см | Ханш 176 см | Дължина 84 см</p>
        <p>Много тънка, удобна и мека, в перфектно състояние.</p>
        <div class="contact">📞 WhatsApp/Viber, телефон</div>
      </div>
    </div>

    <div class="card" data-size="5XL">
      <img src="images/iake.jpg" alt="Яке сатенено">
      <div class="card-content">
        <h3>Електриково зелено яке</h3>
        <p>Размер: 5XL – БГ №56</p>
        <p>Гръдна 126 см | Талия 122 см | Дължина 69 см</p>
        <p>Като ново е, не личи, че е носено. Подходящо за лято/есен.</p>
        <div class="contact">📞 WhatsApp/Viber, телефон</div>
      </div>
    </div>
  </div>

  <script>
    function filterSize(size) {
      const cards = document.querySelectorAll('.card');
      cards.forEach(card => {
        if (size === 'all' || card.dataset.size === size) {
          card.style.display = 'flex';
        } else {
          card.style.display = 'none';
        }
      });
    }
  </script>
</body>
</html>
