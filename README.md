# WifyKonnect
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>WiFyKonnect - Fast, Affordable Internet</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      font-family: 'Inter', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #000000ea;
      color: #171a16cb;
    }
    header {
      background-color: #00d9ffd7;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: white;
      flex-wrap: wrap;
    }
    .logo-container {
      display: flex;
      align-items: center;
    }
    .logo-container img {
      height: 70px;
      width: 70px;
      border-radius: 50%;
      margin-right: 1rem;
      border: 2px solid rgb(7, 243, 7);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      object-fit: cover;
      transition: transform 0.6s ease;
    }
    .logo-container img:hover {
      animation: spin 1.5s linear infinite;
    }
    @keyframes spin {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }
    header h1 {
      margin: 0;
      font-size: 1.8rem;
    }
    nav a {
      margin: 0 1rem;
      color: rgb(6, 8, 160);
      text-decoration: none;
      font-weight: 500;
    }
    .hero {
      position: relative;
      background: url('https://i.postimg.cc/2S9Bj6n1/Whats-App-Image-2025-05-26-at-18-17-02-063f71b3.jpg') no-repeat center center;
      background-size: cover;
      height: 80vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
      color: rgba(245, 243, 243, 0.966);
    }
    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgba(0, 0, 0, 0.53);
      z-index: 1;
    }
    .hero h2,
    .hero p,
    .hero .btn {
      position: relative;
      z-index: 2;
    }
    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      margin-bottom: 2rem;
    }
    .btn {
      background-color: #03c3f3;
      color: white;
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      text-decoration: none;
      cursor: pointer;
      display: inline-block;
      margin-top: 1rem;
      transition: background-color 0.3s ease;
    }
    .btn:hover {
      background-color: #028fcc;
    }
    .plans {
      padding: 2rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }
    .plan {
      background: #07cddbe3;
      border-radius: 8px;
      padding: 1rem;
      box-shadow: 0 2px 6px rgba(53, 250, 4, 0.959);
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .plan:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(247, 248, 248, 0.932);
    }
    .plan h3 {
      margin-top: 0;
      color: #fafafaef;
    }
    .features {
      background: #8eb9b9c9;
      padding: 2rem;
      text-align: center;
    }
    .features h3 {
      color: #f1f5f2de;
    }
    .footer {
      background: #05caece0;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
      flex-wrap: wrap;
    }
    .qr-code {
      height: 80px;
      margin-left: auto;
    }
    @media screen and (max-width: 768px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }
      nav {
        margin-top: 0.5rem;
      }
      .hero {
        padding: 2rem 1rem;
        height: 70vh;
      }
      .hero h2 {
        font-size: 2rem;
      }
      .hero p {
        font-size: 1rem;
      }
      .logo-container img {
        height: 80px;
        width: 80px;
      }
      .footer {
        flex-direction: column;
        align-items: center;
        text-align: center;
      }
      .qr-code {
        margin-top: 1rem;
      }
    }

    /* Modal Styles */
    .modal {
      display: none; /* Hidden by default */
      position: fixed;
      z-index: 1000; /* On top */
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0, 0, 0, 0.7);
      justify-content: center;
      align-items: center;
      padding: 1rem;
    }
    .modal-content {
      background-color: #fff;
      padding: 2rem;
      border-radius: 10px;
      max-width: 400px;
      width: 100%;
      position: relative;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      text-align: center;
    }
    .modal-content h2 {
      margin-top: 0;
      color: #0077cc;
    }
    .modal-content p {
      font-size: 1.2rem;
      margin: 1rem 0 2rem;
    }
    .close-btn {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 1.5rem;
      font-weight: bold;
      color: #aaa;
      cursor: pointer;
      transition: color 0.3s ease;
    }
    .close-btn:hover {
      color: #000;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo-container">
      <img
        src="https://i.postimg.cc/jjqWYsz2/Chat-GPT-Image-May-25-2025-11-34-24-PM.png"
        alt="WiFyKonnect Logo"
      />
      <h1>WiFyKonnect</h1>
    </div>
    <nav>
      <a href="#plans">Available Plans</a>
      <a href="#features">Why WiFyKonnect</a>
      <a href="#contact">Contact Support</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Fast. Reliable. Student-Friendly Wi-Fi.</h2>
    <p>Affordable internet for students, homes, and small businesses in Kenya.</p>
    <a href="#plans" class="btn">View Plans</a>
  </section>

  <section id="plans" class="plans">
    <!-- Example plan with data attributes -->
    <div class="plan">
      <h3>QuickConnect</h3>
      <p>1 Hour 30 Minutes |</p>
      <p><strong>Speed:</strong> 5 Mbps</p>
      <p><strong>Price:</strong> KES 15</p>
      <button class="btn buy-btn" data-plan="QuickConnect" data-price="KES 15">Buy</button>
    </div>
    <div class="plan">
      <h3>SwiftSurf</h3>
      <p>2 Hours |</p>
      <p><strong>Speed:</strong> 7 Mbps</p>
      <p><strong>Price:</strong> KES 35</p>
      <button class="btn buy-btn" data-plan="SwiftSurf" data-price="KES 35">Buy</button>
    </div>
    <div class="plan">
      <h3>FocusBoost</h3>
      <p>6 Hours |</p>
      <p><strong>Speed:</strong> 8 Mbps</p>
      <p><strong>Price:</strong> KES 75</p>
      <button class="btn buy-btn" data-plan="FocusBoost" data-price="KES 75">Buy</button>
    </div>
    <div class="plan">
      <h3>StudyMax</h3>
      <p>12 Hours |</p>
      <p><strong>Speed:</strong> 10 Mbps</p>
      <p><strong>Price:</strong> KES 95</p>
      <button class="btn buy-btn" data-plan="StudyMax" data-price="KES 95">Buy</button>
    </div>
    <div class="plan">
      <h3>ScholarDay</h3>
      <p>24 Hours |</p>
      <p><strong>Speed:</strong> 12 Mbps</p>
      <p><strong>Price:</strong> KES 115</p>
      <button class="btn buy-btn" data-plan="ScholarDay" data-price="KES 115">Buy</button>
    </div>
    <div class="plan">
      <h3>EduWeek</h3>
      <p>7 Days |</p>
      <p><strong>Speed:</strong> 15 Mbps</p>
      <p><strong>Price:</strong> KES 450</p>
      <button class="btn buy-btn" data-plan="EduWeek" data-price="KES 450">Buy</button>
    </div>
    <div class="plan">
      <h3>CampusConnect</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 18 Mbps</p>
      <p><strong>Price:</strong> KES 850</p>
      <button class="btn buy-btn" data-plan="CampusConnect" data-price="KES 850">Buy</button>
    </div>
    <div class="plan">
      <h3>Lite Home</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 20 Mbps</p>
      <p><strong>Price:</strong> KES 1,300</p>
      <button class="btn buy-btn" data-plan="Lite Home" data-price="KES 1,300">Buy</button>
    </div>
    <div class="plan">
      <h3>Smart Home</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 30 Mbps</p>
      <p><strong>Price:</strong> KES 2,500</p>
      <button class="btn buy-btn" data-plan="Smart Home" data-price="KES 2,500">Buy</button>
    </div>
    <div class="plan">
      <h3>Pro Stream</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 50 Mbps</p>
      <p><strong>Price:</strong> KES 5,000</p>
      <button class="btn buy-btn" data-plan="Pro Streams" data-price="KES 5,000">Buy</button>
    </div>
    <div class="plan">
      <h3>Corporate Connect</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 60 Mbps</p>
      <p><strong>Price:</strong> KES 6,000</p>
      <button class="btn buy-btn" data-plan="Corporate Connect" data-price="KES 6,000">Buy</button>
    </div>
    <div class="plan">
      <h3>Enterprise Elite</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 70 Mbps</p>
      <p><strong>Price:</strong> KES 7,200</p>
      <button class="btn buy-btn" data-plan="Enterprise Elite" data-price="KES 7,200">Buy</button>
    </div>
    <div class="plan">
      <h3>Ultra Business</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 80 Mbps</p>
      <p><strong>Price:</strong> KES 9,000</p>
      <button class="btn buy-btn" data-plan="Ultra Business" data-price="KES 9,000">Buy</button>
    </div>
    <div class="plan">
      <h3>Unlimited Pro</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 75 Mbps</p>
      <p><strong>Price:</strong> KES 10,000</p>
      <button class="btn buy-btn" data-plan="Unlimited Pro" data-price="KES 10,000">Buy</button>
    </div>
    <div class="plan">
      <h3>Unlimited Elite</h3>
      <p>30 Days |</p>
      <p><strong>Speed:</strong> 100 Mbps</p>
      <p><strong>Price:</strong> KES 15,000</p>
      <button class="btn buy-btn" data-plan="Unlimited Elite" data-price="KES 15,000">Buy</button>
    </div>
    </section>

  <section id="features" class="features">
    <h3>Why Choose WiFyKonnect?</h3>
    <p>
      Student Plans – Pocket-friendly<br />
      5 Mbps Minimum Speeds Guaranteed<br />
      Easy Payments via M-Pesa<br />
      Secure Login – Hotspot & PPPoE<br />
      Always Available – 24/7 Internet
    </p>
  </section>

  <section id="contact" class="features">
    <h3>Contact Us</h3>
    <p>
      📱 WhatsApp:
      <a href="https://wa.me/254791808215" target="_blank" style="color: white;">Chat Now</a><br />
      💳 M-Pesa Buy Goods and Services: <strong>5375801</strong><br />
      📧 Email: wiflyglobal@gmail.com<br />
      📍 Location: Nairobi, Kenya
    </p>
  </section>

  <footer class="footer">
    <p>&copy; 2025 WiFyKonnect Internet. All rights reserved.</p>
    <img
      src="https://api.qrserver.com/v1/create-qr-code/?size=80x80&data=https://wifykonnect.co.ke"
      alt="WiFyKonnect QR Code"
      class="qr-code"
    />
  </footer>

  <!-- Modal -->
  <div id="purchaseModal" class="modal">
    <div class="modal-content">
      <span class="close-btn">&times;</span>
      <h2 id="modalPlanName">Plan Name</h2>
      <p id="modalPlanPrice">Price: </p>
      <button id="confirmPurchaseBtn" class="btn">Confirm Purchase</button>
    </div>
  </div>

  <script>
    const modal = document.getElementById('purchaseModal');
    const modalPlanName = document.getElementById('modalPlanName');
    const modalPlanPrice = document.getElementById('modalPlanPrice');
    const closeBtn = document.querySelector('.close-btn');
    const confirmBtn = document.getElementById('confirmPurchaseBtn');
    const buyButtons = document.querySelectorAll('.buy-btn');

    buyButtons.forEach(button => {
      button.addEventListener('click', () => {
        const plan = button.getAttribute('data-plan');
        const price = button.getAttribute('data-price');
        modalPlanName.textContent = plan;
        modalPlanPrice.textContent = `Price: ${price}`;
        modal.style.display = 'flex';
      });
    });

    closeBtn.addEventListener('click', () => {
      modal.style.display = 'none';
    });

    confirmBtn.addEventListener('click', () => {
      alert('Thank you for your purchase! (Functionality to be implemented)');
      modal.style.display = 'none';
    });

    window.addEventListener('click', (e) => {
      if (e.target === modal) {
        modal.style.display = 'none';
      }
    });
  </script>
</body>
</html>
