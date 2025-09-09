
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sam Adedams Portfolio</title>
  <style>
    :root {
      --blue: #1e3a8a;
      --grey: #f3f4f6;
      --dark-grey: #374151;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--grey);
      color: var(--dark-grey);
    }
    header {
      background-color: var(--blue);
      color: white;
      padding: 2rem;
      text-align: center;
      position: relative;
    }
    .tagline {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
      position: relative;
    }
    .underline {
      width: 100px;
      height: 4px;
      background-color: white;
      margin: 0 auto;
      animation: moveUnderline 2s infinite ease-in-out;
    }
    @keyframes moveUnderline {
      0% { transform: translateX(0); }
      50% { transform: translateX(20px); }
      100% { transform: translateX(0); }
    }
    nav {
      background-color: var(--dark-grey);
      display: flex;
      justify-content: center;
      gap: 2rem;
      padding: 1rem;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 2rem;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      color: var(--blue);
      margin-bottom: 1rem;
    }
    .portfolio-item {
      margin-bottom: 1rem;
    }
    .testimonial {
      background-color: white;
      padding: 1rem;
      margin-bottom: 1rem;
      border-left: 4px solid var(--blue);
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    input, textarea {
      padding: 0.5rem;
      border: 1px solid var(--dark-grey);
      border-radius: 4px;
    }
    button {
      background-color: var(--blue);
      color: white;
      border: none;
      padding: 0.75rem;
      cursor: pointer;
      border-radius: 4px;
    }
    footer {
      background-color: var(--dark-grey);
      color: white;
      text-align: center;
      padding: 2rem 1rem;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .footer-img {
      width: 120px;
      height: auto;
      border-radius: 8px;
      margin-bottom: 1rem;
    }
  </style>
</head>
<body>

  <header>
    <h1>Sam Adedams</h1>
    <p class="tagline">Full Stack Developer | Graphics Designer | Brand Marketer</p>
    <div class="underline"></div>
  </header>

  <nav>
    <a href="#about">About</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="about">
    <h2>About Me</h2>
    <p>I’m Sam Adedams, a creative technologist blending full-stack development, graphic design, and brand marketing to build digital experiences that resonate. I help businesses grow by crafting intuitive websites and compelling brand identities.</p>
  </section>

  <section id="portfolio">
    <h2>Portfolio</h2>
    <div class="portfolio-item">
      <strong>dGlobalGrowthField</strong><br />
      <a href="https://www.dglobalgrowthfield.com" target="_blank">www.dglobalgrowthfield.com</a>
    </div>
    <div class="portfolio-item">
      <strong>OddMenu</strong><br />
      <a href="https://www.oddmenu.com" target="_blank">www.oddmenu.com</a>
    </div>
    <div class="portfolio-item">
      <strong>Adedams Tech Hub</strong><br />
      <a href="https://sr678.github.io/Adedams-tech-hub" target="_blank">Adedams-tech-hub</a>
    </div>
  </section>

  <section id="testimonials">
    <h2>Testimonials</h2>
    <div class="testimonial">
      “Sam transformed our brand presence online. His designs are intuitive and his development skills are top-notch.”  
      <br /><em>— Mr. Adedapo Bello, CEO, D-globalgrowthfield</em>
    </div>
    <div class="testimonial">
      “Working with Sam was seamless. He understood our vision and delivered a product that exceeded expectations.”  
      <br /><em>— Olga Ivanova, Product Manager, OddMenu</em>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <form id="contactForm">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <input type="text" name="subject" placeholder="Subject" required />
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
    <p id="formResponse" style="margin-top:1rem;"></p>
  </section>

  <footer>
    <img src="your-image.jpg" alt="Sam Adedams" class="footer-img" />
    <p>© 2025 Sam Adedams. All rights reserved.</p>
  </footer>

  <script>
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const formResponse = document.getElementById('formResponse');
      formResponse.textContent = "Thanks for reaching out! I'll get back to you soon.";
      this.reset();
    });
  </script>

</body>
</html>
