<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Samgbemex Services</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 2rem; background: #f9f9f9; color: #333; }
    .dark-mode { background: #121212; color: #eee; }
    form { margin-bottom: 2rem; }
    input, textarea, button { display: block; margin: 0.5rem 0; padding: 0.5rem; width: 100%; max-width: 400px; }
    .testimonial-card { background: #fff; padding: 1rem; margin: 1rem 0; border-left: 4px solid #007BFF; }
    .testimonial-list { margin-top: 1rem; }
    button { background: #007BFF; color: white; border: none; cursor: pointer; }
    button:hover { background: #0056b3; }
  </style>
</head>
<body>

  <h1>Welcome to Samgbemex Services</h1>
  <button onclick="toggleDarkMode()">🌙 Toggle Dark Mode</button>

  <!-- 📩 Contact Form -->
  <h2>Contact Us</h2>
  <form id="contact-form">
    <input type="text" placeholder="Your Name" required />
    <input type="email" placeholder="Your Email" required />
    <textarea placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
  </form>

  <!-- 📅 Appointment Booking -->
  <h2>Book an Appointment</h2>
  <form id="appointment-form">
    <input type="text" id="client-name" placeholder="Your Name" required />
    <input type="email" id="client-email" placeholder="Your Email" required />
    <input type="date" id="appointment-date" required />
    <input type="time" id="appointment-time" required />
    <button type="submit">Book Appointment</button>
  </form>
  <div id="confirmation"></div>

  <!-- 💬 Testimonial Submission -->
  <h2>Share Your Testimonial</h2>
  <form id="testimonial-form">
    <input type="text" id="testimonial-author" placeholder="Your Name" required />
    <textarea id="testimonial-text" placeholder="Your Testimonial" required></textarea>
    <button type="submit">Submit Testimonial</button>
  </form>

  <!-- 💬 Testimonials Display -->
  <h2>What Our Clients Say</h2>
  <div class="testimonial-list"></div>

  <!-- 🔌 Firebase SDK -->
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-app.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.6.1/firebase-firestore.js"></script>

  <!-- 📬 EmailJS SDK -->
  <script src="https://cdn.emailjs.com/dist/email.min.js"></script>

  <!-- ⚙️ JavaScript Logic -->
  <script>
    // 🌙 Dark Mode
    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }

    // 📩 Contact Form
    document.getElementById('contact-form').addEventListener('submit', function (e) {
      e.preventDefault();
      alert('Thanks for reaching out, Sam will get back to you soon!');
      this.reset();
    });

    // 🔧 Firebase Config
    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_PROJECT_ID.appspot.com",
      messagingSenderId: "YOUR_SENDER_ID",
      appId: "YOUR_APP_ID"
    };
    const app = firebase.initializeApp(firebaseConfig);
    const db = firebase.firestore();

    // 📬 EmailJS Init
    emailjs.init("YOUR_PUBLIC_KEY");

    // 📅 Appointment Booking
    document.getElementById('appointment-form').addEventListener('submit', function (e) {
      e.preventDefault();

      const name = document.getElementById('client-name').value;
      const email = document.getElementById('client-email').value;
      const date = document.getElementById('appointment-date').value;
      const time = document.getElementById('appointment-time').value;

      // Save to Firebase
      db.collection("appointments").add({ name, email, date, time, timestamp: new Date() })
        .then(() => console.log("Saved to Firebase"))
        .catch(err => console.error("Firebase error:", err));

      // Send Email
      emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", { name, email, date, time })
        .then(() => {
          document.getElementById('confirmation').innerHTML =
            `✅ Appointment booked for <strong>${name}</strong> on <strong>${date}</strong> at <strong>${time}</strong>. Confirmation sent to <strong>${email}</strong>.`;
          this.reset();
        })
        .catch(error => {
          alert("❌ Email failed to send.");
          console.error(error);
        });
    });

    // 💬 Testimonials
    const testimonials = [];

    document.getElementById('testimonial-form').addEventListener('submit', function (e) {
      e.preventDefault();

      const author = document.getElementById('testimonial-author').value;
      const text = document.getElementById('testimonial-text').value;

      testimonials.push({ quote: text, author });

      document.querySelector('.testimonial-list').innerHTML = testimonials.map(t => `
        <div class="testimonial-card">
          <p>"${t.quote}"</p>
          <h4>- ${t.author}</h4>
        </div>
      `).join('');

      this.reset();
    });
  </script>
</body>
</html>
