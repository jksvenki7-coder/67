# 67<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group of Business</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: white;
    color: #024a86;
  }
  header {
    background: #87ceeb;
    padding: 10px 20px;
    text-align: center;
    color: white;
    font-size: 26px;
    font-weight: bold;
  }
  nav {
    background: #e1efff;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    border-bottom: 2px solid #87ceeb;
  }
  nav button {
    background: transparent;
    border: none;
    color: #024a86;
    font-size: 16px;
    margin: 8px 12px;
    padding: 10px 14px;
    cursor: pointer;
    border-radius: 6px;
    transition: background-color 0.3s ease;
  }
  nav button:hover,
  nav button.active {
    background: #024a86;
    color: white;
  }
  section {
    max-width: 900px;
    margin: 20px auto;
    padding: 10px 20px;
    display: none;
    border-radius: 8px;
    box-shadow: 0 0 10px #c0deff;
    background: #f9fbff;
  }
  section.active {
    display: block;
  }
  h2 {
    color: #024a86;
  }
  form label {
    display: block;
    margin-top: 10px;
    font-weight: bold;
  }
  form input, form textarea, form select, form button {
    width: 100%;
    padding: 8px;
    margin-top: 4px;
    border: 1px solid #87ceeb;
    border-radius: 5px;
    font-size: 14px;
  }
  form button {
    margin-top: 14px;
    background: #024a86;
    color: white;
    border: none;
    cursor: pointer;
    font-weight: bold;
    transition: background 0.3s ease;
  }
  form button:hover {
    background: #0160a9;
  }
  #map {
    height: 300px;
    width: 100%;
    margin-top: 10px;
    border-radius: 8px;
    border: 1px solid #87ceeb;
  }
  .whatsapp-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25d366;
    color: white;
    border: none;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    font-size: 30px;
    cursor: pointer;
    box-shadow: 0 0 10px #25d366cc;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .camera-section video, .camera-section canvas {
    width: 100%;
    max-width: 400px;
    border-radius: 8px;
    margin-top: 10px;
    background: black;
  }
  .camera-section button {
    margin-top: 10px;
    background: #87ceeb;
    color: #024a86;
    border: none;
    padding: 8px 12px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
  }
  @media (max-width: 600px) {
    nav {
      flex-direction: column;
    }
    nav button {
      margin: 6px 0;
    }
  }
</style>
</head>
<body>
<header>JKS Group of Business</header>
<nav>
  <button class="nav-btn active" data-target="ecommerce">E-Commerce</button>
  <button class="nav-btn" data-target="events">Events & Catering</button>
  <button class="nav-btn" data-target="courier">Courier & Ride Booking</button>
  <button class="nav-btn" data-target="jobs">Job Consultancy</button>
  <button class="nav-btn" data-target="loans">Loans & Insurance</button>
  <button class="nav-btn" data-target="tours">Tours & Travels</button>
  <button class="nav-btn" data-target="realestate">Real Estate</button>
  <button class="nav-btn" data-target="homeservices">Home Services</button>
  <button class="nav-btn" data-target="investment">Investment Services</button>
  <button class="nav-btn" data-target="location">Location Map</button>
  <button class="nav-btn" data-target="camera">Camera Access</button>
</nav>

<section id="ecommerce" class="active">
  <h2>E-Commerce</h2>
  <p>Buy quality products from Shree Ram brand. Fill details to order.</p>
  <form id="ecommerceForm">
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Order Details</label><textarea rows="3" required></textarea>
    <label>Delivery Address</label><textarea rows="3" required></textarea>
    <button type="submit">Place Order</button>
  </form>
</section>

<section id="events">
  <h2>Events & Catering</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Event Details</label><textarea rows="3" required></textarea>
    <label>Event Address</label><textarea rows="3" required></textarea>
    <button type="submit">Request Booking</button>
  </form>
</section>

<section id="courier">
  <h2>Courier & Ride Booking</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Pickup Address</label><textarea rows="2" required></textarea>
    <label>Drop Address</label><textarea rows="2" required></textarea>
    <label>Service Type</label>
    <select required>
      <option value="">Select Service</option>
      <option>Courier</option>
      <option>Ride</option>
    </select>
    <button type="submit">Book Now</button>
  </form>
</section>

<section id="jobs">
  <h2>Job Consultancy</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Skills / Profession</label><input type="text" required placeholder="e.g. IT, Sales" />
    <label>Experience (Years)</label><input type="number" min="0" max="50" required />
    <button type="submit">Register</button>
  </form>
</section>

<section id="loans">
  <h2>Loans & Insurance</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Loan / Insurance Type</label>
    <select required>
      <option value="">Select Type</option>
      <option>Personal Loan</option>
      <option>Home Loan</option>
      <option>Vehicle Loan</option>
      <option>Life Insurance</option>
      <option>Health Insurance</option>
    </select>
    <label>Amount (approx.)</label><input type="number" min="0" required />
    <button type="submit">Apply Now</button>
  </form>
</section>

<section id="tours">
  <h2>Tours & Travels</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Destination</label><input type="text" required />
    <label>Travel Dates</label><input type="text" placeholder="Start - End" required />
    <button type="submit">Plan Trip</button>
  </form>
</section>

<section id="realestate">
  <h2>Real Estate</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Property Type</label>
    <select required>
      <option value="">Select Type</option>
      <option>Sale</option>
      <option>Rent</option>
    </select>
    <label>Property Details</label><textarea rows="3" placeholder="Location, size, price, etc." required></textarea>
    <button type="submit">Submit Inquiry</button>
  </form>
</section>

<section id="homeservices">
  <h2>Home Services</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Service Required</label>
    <select required>
      <option value="">Select Service</option>
      <option>CCTV Installation</option>
      <option>Mobile Repair</option>
      <option>Electrical Work</option>
      <option>Plumbing</option>
      <option>Cleaning</option>
    </select>
    <label>Service Address</label>
    <textarea rows="3" required></textarea>
    <button type="submit">Request Service</button>
  </form>
</section>

<section id="investment">
  <h2>Investment Services</h2>
  <form>
    <label>Name</label><input type="text" required />
    <label>Mobile Number</label><input type="tel" pattern="[0-9]{10}" required />
    <label>Investment Interest</label>
    <select required>
      <option value="">Select Type</option>
      <option>Mutual Funds</option>
      <option>Stocks</option>
      <option>Real Estate</option>
      <option>Fixed Deposits</option>
      <option>Other</option>
    </select>
    <button type="submit">Get Consultation</button>
  </form>
</section>

<section id="location">
  <h2>Our Location</h2>
  <p>Find us on the map below.</p>
  <div id="map"></div>
</section>

<section id="camera" class="camera-section">
  <h2>Camera Access (for Orders / Scanning)</h2>
  <video id="video" autoplay playsinline></video>
  <canvas id="canvas" style="display:none;"></canvas>
  <button id="snap">Take Photo</button>
  <button id="uploadPhoto" style="display:none;">Upload Photo</button>
  <p id="photoStatus"></p>
</section>

<button class="whatsapp-button" title="Order via WhatsApp" onclick="openWhatsApp()" aria-label="WhatsApp order button">&#x1F4AC;</button>

<script>
  const navButtons = document.querySelectorAll('nav .nav-btn');
  const sections = document.querySelectorAll('section');

  navButtons.forEach(button => {
    button.addEventListener('click', () => {
      navButtons.forEach(btn => btn.classList.remove('active'));
      sections.forEach(sec => sec.classList.remove('active'));
      button.classList.add('active');
      document.getElementById(button.dataset.target).classList.add('active');
    });
  });

  function openWhatsApp() {
    const message = encodeURIComponent('Hello JKS Group of Business, I want to place an order. Please assist.');
    const number = '918977143043';
    window.open(`https://wa.me/${number}?text=${message}`, '_blank');
  }

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', e => {
      e.preventDefault();
      alert('Thank you for your submission! We will contact you shortly.');
      form.reset();
    });
  });

  function initMap() {
    const location = { lat: 17.385044, lng: 78.486671 };
    const map = new google.maps.Map(document.getElementById('map'), {
      zoom: 12,
      center: location,
    });
    new google.maps.Marker({
      position: location,
      map,
      title: 'JKS Group of Business',
    });
  }

  function loadGoogleMaps() {
    const script = document.createElement('script');
    script.src = 'https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap';
    script.defer = true;
    document.head.appendChild(script);
  }
  loadGoogleMaps();

  const video = document.getElementById('video');
  const canvas = document.getElementById('canvas');
  const snapBtn = document.getElementById('snap');
  const uploadBtn = document.getElementById('uploadPhoto');
  const photoStatus = document.getElementById('photoStatus');

  async function setupCamera() {
    try {
      const stream = await navigator.mediaDevices.getUserMedia({ video: true });
      video.srcObject = stream;
    } catch {
      photoStatus.textContent = 'Camera access denied or unavailable.';
    }
  }
  setupCamera();

  snapBtn.addEventListener('click', () => {
    canvas.width = video.videoWidth;
    canvas.height = video.videoHeight;
    canvas.getContext('2d').drawImage(video, 0, 0, canvas.width, canvas.height);
    canvas.style.display = 'block';
    uploadBtn.style.display = 'inline-block';
    photoStatus.textContent = 'Photo taken. Click upload to send.';
  });

  uploadBtn.addEventListener('click', () => {
    const imageData = canvas.toDataURL('image/png');
    photoStatus.textContent = 'Photo uploaded successfully! Thank you.';
    uploadBtn.style.display = 'none';
    canvas.style.display = 'none';
  });
</script>
</body>
</html>
