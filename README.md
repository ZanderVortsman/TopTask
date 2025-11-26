# TopTask
TopTask website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TopTask Car Service</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: #fff;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 50px 20px;
      background: rgba(0,0,0,0.5);
      animation: fadeInDown 1s ease;
    }

    header h1 {
      font-size: 3rem;
      margin: 0;
    }

    header p {
      font-size: 1.2rem;
      margin-top: 10px;
    }

    nav {
      text-align: center;
      margin: 20px 0;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #ffd700;
    }

    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 40px 20px;
      text-align: center;
    }

    .service-card {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      border-radius: 15px;
      transition: transform 0.3s;
      animation: fadeIn 1s ease;
    }

    .service-card:hover {
      transform: scale(1.05);
      background: rgba(255,255,255,0.2);
    }

    .service-card h3 {
      margin-top: 0;
    }

    .book-now {
      text-align: center;
      margin: 50px 0;
    }

    .book-now button {
      background: #ffd700;
      color: #000;
      border: none;
      padding: 15px 30px;
      font-size: 1.2rem;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s, background 0.3s;
    }

    .book-now button:hover {
      background: #ffbf00;
      transform: scale(1.1);
    }

    .form-container {
      display: none;
      text-align: center;
      padding: 20px;
    }

    .form-container form {
      display: inline-block;
      background: rgba(0,0,0,0.6);
      padding: 30px;
      border-radius: 15px;
      text-align: left;
      animation: fadeInUp 1s ease;
    }

    .form-container label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }

    .form-container input, 
    .form-container select, 
    .form-container textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: none;
    }

    .form-container button {
      width: 100%;
      background: #ffd700;
      color: #000;
      padding: 15px;
      font-size: 1rem;
      border-radius: 10px;
      border: none;
      cursor: pointer;
      transition: transform 0.3s, background 0.3s;
    }

    .form-container button:hover {
      background: #ffbf00;
      transform: scale(1.05);
    }

    footer {
      text-align: center;
      padding: 20px;
      background: rgba(0,0,0,0.5);
      margin-top: 50px;
    }

    @media(max-width: 600px) {
      header h1 {
        font-size: 2rem;
      }
    }

    /* Animations */
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-50px);}
      to { opacity: 1; transform: translateY(0);}
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(50px);}
      to { opacity: 1; transform: translateY(0);}
    }

    @keyframes fadeIn {
      from { opacity: 0;}
      to { opacity: 1;}
    }
  </style>
</head>
<body>

  <header>
    <h1>TopTask Car Service</h1>
    <p>Your trusted car repair and maintenance experts.</p>
  </header>

  <nav>
    <a href="#services">Services</a>
    <a href="#book">Book Now</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="services" class="services">
    <div class="service-card">
      <h3>Oil Change</h3>
      <p>Keep your engine running smoothly with our oil change services.</p>
    </div>
    <div class="service-card">
      <h3>Repair</h3>
      <p>Professional repairs for all types of vehicles, ensuring safety and reliability.</p>
    </div>
    <div class="service-card">
      <h3>Engine Diagnostics</h3>
      <p>Identify and fix engine issues with our advanced diagnostics tools.</p>
    </div>
    <div class="service-card">
      <h3>General Maintenance</h3>
      <p>Regular maintenance to prolong your vehicle's lifespan and performance.</p>
    </div>
  </section>

  <section id="book" class="book-now">
    <button onclick="toggleForm()">Book Your Service</button>
    <div class="form-container" id="bookingForm">
      <form onsubmit="sendWhatsApp(event)">
        <label for="name">Your Name</label>
        <input type="text" id="name" name="name" required>

        <label for="vehicle">Vehicle Make & Model</label>
        <input type="text" id="vehicle" name="vehicle" required>

        <label for="engine">Engine Size</label>
        <input type="text" id="engine" name="engine" placeholder="e.g. 1.6L" required>

        <label for="fuel">Fuel Type</label>
        <select id="fuel" name="fuel" required>
          <option value="">Select fuel type</option>
          <option value="Petrol">Petrol</option>
          <option value="Diesel">Diesel</option>
        </select>

        <label for="service">Service Needed</label>
        <select id="service" name="service" required>
          <option value="">Select a service</option>
          <option value="Oil Change">Oil Change</option>
          <option value="Repair">Repair</option>
          <option value="Engine Diagnostics">Engine Diagnostics</option>
          <option value="General Maintenance">General Maintenance</option>
        </select>

        <label for="details">Additional Details</label>
        <textarea id="details" name="details" rows="3" placeholder="Anything else we should know?"></textarea>

        <button type="submit">Submit via WhatsApp</button>
      </form>
    </div>
  </section>

  <footer id="contact">
    <p>Contact us: 066 230 6384 | &copy; 2025 TopTask Car Service</p>
  </footer>

  <script>
    function toggleForm() {
      const form = document.getElementById('bookingForm');
      form.style.display = form.style.display === 'block' ? 'none' : 'block';
      window.scrollTo({ top: form.offsetTop, behavior: 'smooth' });
    }

    function sendWhatsApp(e) {
      e.preventDefault();
      const name = document.getElementById('name').value;
      const vehicle = document.getElementById('vehicle').value;
      const engine = document.getElementById('engine').value;
      const fuel = document.getElementById('fuel').value;
      const service = document.getElementById('service').value;
      const details = document.getElementById('details').value;

      const message = `Hello, my name is ${name}. I need the following service: ${service} for my ${vehicle} (${engine}, ${fuel}). Additional details: ${details}`;
      const phone = '27662306384'; // WhatsApp number with country code
      const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;

      // Works on desktop and mobile
      window.open(url, '_blank');
    }
  </script>

</body>
</html>