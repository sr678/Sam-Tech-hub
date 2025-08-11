<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sam Adedams | Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background-color: #f4f4f4;
      color: #333;
    }

    header {
      background: #333;
      color: #fff;
      padding: 1rem 2rem;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 1rem;
    }

    .nav-links a {
      color: #fff;
      text-decoration: none;
    }

    .hero {
      background: linear-gradient(to right, #6a11cb, #2575fc);
      color: #fff;
      padding: 5rem 2rem;
      text-align: center;
    }

    .btn {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background: #fff;
      color: #2575fc;
      border-radius: 5px;
      text-decoration: none;
    }

    .section {
      padding: 4rem 2rem;
      background: #fff;
    }

    .project-list {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
    }

    .project-card {
      background: #eee;
      padding: 1rem;
      border-radius: 8px;
      flex: 1 1 300px;
    }

    .testimonial-list {
      display: flex;
      flex-direction: column;
      gap: 2rem;
      max-width: 800px;
      margin: auto;
    }

    .testimonial-card {
      background: #f9f9f9;
      padding: 1.5rem;
      border-left: 5px solid #2575fc;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .testimonial-card h4 {
      margin-top: 1rem;
      font-weight: normal;
      color: #555;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      max-width: 500px;
      margin: auto;
    }

    input, textarea {
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    button {
      padding: 0.75rem;
      background: #2575fc;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    #confirmation {
      margin-top: 1rem;
      color: green;
      text-align: center;
    }

    footer {
      text-align: center;
      padding: 2rem;
      background: #333;
      color: #fff;
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <h1 class="logo">Sam Adedams</h1>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#appointment">Book</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h2>Hello, I'm Sam Adedams</h2>
    <p>Web Developer | Graphics Designer | Brand Marketer</p>
    <a href="#projects" class="btn">Explore My Work</a>
  </section>

  <section id="about" class="section">
    <h2>About Me</h2>
    <p>
      I'm a creative professional with a passion for building engaging digital experiences.
      With expertise in web development, graphic design, and brand marketing, I help businesses grow and connect with their audience.
      Currently working at <strong>DGGlobalGrowthField</strong> since 2021.
    </p>
  </section>

  <section id="projects" class="section">
    <h2>Projects</h2>
    <div class="project-list">
      <div class="project-card">
        <h3>Brand Identity for Samgbemex Enterprise</h3>
        <p>Created a cohesive brand identity including logo, typography, and visual assets to elevate Samgbemex’s market presence.</p>
      </div>
      <div class="project-card">
        <h3>Responsive Website for DGGlobalGrowthField</h3>
        <p>Designed and developed a fully responsive website optimized for performance, accessibility, and user engagement.</p>
      </div>
      <div class="project-card">
        <h3>Brand Identity for XYZ</h3>
        <p>Developed a full brand identity including logo, color palette, and marketing assets.</p>
      </div>
      <div class="project-card">
        <h3>Responsive Website for ABC</h3>
        <p>Designed and built a responsive website with optimized UX and SEO.</p>
      </div>
    </div>
  </section>

  <section id="testimonials" class="section">
    <h2>Testimonials</h2>
    <div class="testimonial-list">
      <div class="testimonial-card">
        <p>"Sam's creativity and professionalism transformed our brand. Highly recommended!"</p>
        <h4>- CEO, Samgbemex Enterprise</h4>
      </div>
      <div class="testimonial-card">
        <p>"The website Sam built for us is sleek, fast, and user-friendly. Our traffic has doubled!"</p>
        <h4>- Marketing Lead, DGGlobalGrowthField</h4>
      </div>
    </div>
  </section>

  <section id="contact" class="section">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <section id="appointment" class="section">
    <h2>Book an Appointment</h2>
    <form id="appointment-form">
      <input type="text" id="client-name" placeholder="Your Name" required />
      <input type="email" id="client-email" placeholder="Your Email" required />
      <input type="date" id="appointment-date" required />
      <input type="time" id="appointment-time" required />
      <button type="submit">Book Appointment</button>
    </form>
    <div id="confirmation"></div>
  </section>

  <footer>
    <p>&copy; 2025 Sam Adedams. All rights reserved.</p>
  </footer>

  <script>
    document.getElementById('contact-form').addEventListener('submit', function (e) {
      e.preventDefault();
      alert('Thanks for reaching out, Sam will get back to you soon!');
    });

    document.getElementById('appointment-form').addEventListener('submit', function (e) {
      e.preventDefault();

      const name = document.getElementById('client-name').value;
      const email = document.getElementById('client-email').value;
      const date = document.getElementById('appointment-date').value;
      const time = document.getElementById('appointment-time').value;

      const confirmation = document.getElementById('confirmation');
      confirmation.innerHTML = `✅ Appointment booked for <strong>${name}</strong> on <strong>${date}</strong> at <strong>${time}</strong>. A confirmation will be sent to <strong>${email}</strong>.`;

      document.getElementById('appointment-form').reset();
    });
  </script>
</body>
</html>
