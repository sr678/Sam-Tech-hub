<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sam Adedams | Portfolio</title>
  <style>
    :root {
      --primary-color: #007BFF;
      --secondary-color: #6c757d;
      --background-light: #f8f9fa;
      --text-dark: #212529;
      --accent-purple: #6a1b9a;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: var(--background-light);
      color: var(--text-dark);
    }

    .social-bar {
      position: fixed;
      top: 0;
      right: 0;
      background: var(--accent-purple);
      padding: 0.5rem;
      display: flex;
      gap: 0.5rem;
      z-index: 1000;
    }

    .social-bar img {
      width: 24px;
      height: 24px;
      filter: brightness(0) invert(1);
      cursor: pointer;
      transition: transform 0.3s;
    }

    .social-bar img:hover {
      transform: scale(1.1);
    }

    .hero {
      background: var(--primary-color);
      color: #fff;
      text-align: center;
      padding: 3rem 1rem;
      margin-top: 2.5rem;
    }

    .brand-name {
      font-size: 2.5rem;
      font-weight: bold;
      color: var(--accent-purple);
      margin: 0.5rem 0;
    }

    .underline {
      width: 120px;
      height: 8px;
      background: gold;
      margin: 0 auto 1rem;
      border-radius: 4px;
    }

    .profile-img {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      margin: 1rem auto;
      display: block;
      border: 4px solid #fff;
      object-fit: cover;
    }

    #animated-title {
      font-size: 1.3rem;
      font-weight: bold;
      height: 2rem;
      overflow: hidden;
      white-space: nowrap;
      border-right: 2px solid #fff;
      animation: blink-caret 0.75s step-end infinite;
    }

    @keyframes blink-caret {
      from, to { border-color: transparent; }
      50% { border-color: white; }
    }

    .hire-btn {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background: var(--secondary-color);
      color: #fff;
      text-decoration: none;
      border-radius: 5px;
      transition: background 0.3s;
    }

    .hire-btn:hover {
      background: #5a6268;
    }

    section {
      padding: 2rem;
      max-width: 800px;
      margin: auto;
    }

    section h2 {
      color: var(--primary-color);
      margin-bottom: 1rem;
      text-align: center;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    li {
      margin-bottom: 1.5rem;
      background: #fff;
      padding: 1rem;
      border-left: 5px solid var(--primary-color);
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    }

    a {
      color: var(--primary-color);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    #testimonials {
      padding: 2rem;
      background: #fff;
      text-align: center;
    }

    .testimonial-box {
      background: var(--secondary-color);
      color: #fff;
      margin: 1rem auto;
      padding: 1rem 2rem;
      border-radius: 8px;
      max-width: 700px;
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1s ease, transform 1s ease;
    }

    .testimonial-box.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .testimonial-box h4 {
      margin-top: 1rem;
      font-weight: normal;
      font-style: italic;
    }

    #contact {
      text-align: center;
      padding: 2rem;
      background: var(--primary-color);
      color: #fff;
    }

    #contact a {
      color: #fff;
      font-weight: bold;
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 1rem;
      background: var(--secondary-color);
      color: #fff;
    }
  </style>
</head>
<body>
  <div class="social-bar">
    <a href="https://x.com/@SamDigitalHub" target="_blank" title="X (Twitter)">
      <img src="x-icon.png" alt="X" />
    </a>
    <a href="https://linkedin.com/in/SamAdedams" target="_blank" title="LinkedIn">
      <img src="linkedin-icon.png" alt="LinkedIn" />
    </a>
    <a href="https://linktr.ee/SamdigitalHub" target="_blank" title="Linktree">
      <img src="link-icon.png" alt="Linktree" />
    </a>
    <a href="#" title="Menu">
      <img src="menu-icon.png" alt="Menu" />
    </a>
  </div>

  <header class="hero">
    <h1>Hey, Welcome to my page, I am...</h1>
    <h2 class="brand-name">Sam Adedams</h2>
    <div class="underline"></div>
    <img src=IMG_20240602_094643_742.jpg alt="Sam's Profile" class="profile-img" />
    <h3 id="animated-title"></h3>
    <a href="mailto:samadedamola4@gmail.com" class="hire-btn">Hire Me</a>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>
      I'm a multi-disciplinary technocrat passionate about building scalable web solutions, crafting compelling visuals, and elevating brands through strategic marketing. I specialize in full-stack development, graphic design, and brand strategy.
    </p>
    <p><a href="https://linktr.ee/SamdigitalHub" target="_blank">Visit My Linktree</a></p>
  </section>

  <section id="projects">
    <h2>Project Showcase</h2>
    <ul>
      <li>
        <strong>D-GlobalGrowthField</strong> – Collaborated to build a user-friendly website<br />
        <a href="https://www.dglobalgrowthfield.com" target="_blank">Visit Site</a>
      </li>
      <li>
        <strong>OddMenu</strong> – UX-focused food discovery platform<br />
        <a href="https://www.oddmenu.com" target="_blank">Visit Site</a>
      </li>
      <li>
        <strong>Rome2Rio</strong> – Contributed to interface enhancements<br />
        <a href="https://www.rome2rio.com" target="_blank">Visit Site</a>
      </li>
    </ul>
  </section>

  <section id="testimonials">
    <h2>Testimonials</h2>
    <div class="testimonial-box">
      <p>"Sam is a visionary developer. He transformed our brand presence online with precision and creativity."</p>
      <h4>— D-GlobalGrowthField Team</h4>
    </div>
    <div class="testimonial-box">
      <p>"Working with Sam was seamless. His design instincts and marketing strategy helped us scale fast."</p>
      <h4>— OddMenu Founder</h4>
    </div>
    <div class="testimonial-box">
      <p>"Sam’s full-stack skills and branding insights are unmatched. Highly recommended."</p>
      <h4>— Rome2Rio UX Lead</h4>
    </div>
  </section>

  <section id="contact">
    <h2>Let's Talk</h2>
    <p>Interested in working together or have a project in mind?</p>
    <p>Email me at <a href="mailto:samadedamola4@gmail.com">samadedamola4@gmail.com</a></p>
  </section>

  <footer>
    <p>© 2025 Sam Adedams | All rights reserved</p>
  </footer>

  <script>
    //[43dcd9a7-70db-4a1f-b0ae-981daa162054](https://github.com/Ronnie434/30-days-of-React/tree/22142106cb46f717a1259f84227cc90ed7fe50cc/02_Day_Introduction_to_React%2F02_introduction_to_react.md?citationMarker=43dcd9a7-70db-4a1f-b0ae-981daa162054 "1")
<script>
    // Typewriter animation
    const titles = [
      "Full Stack Developer",
      "Graphics Designer",
      "Brand Marketer"
    ];

    let titleIndex = 0;
    let charIndex = 0;
    const speed = 100;
    const target = document.getElementById("animated-title");

    function typeTitle() {
      if (charIndex < titles[titleIndex].length) {
        target.textContent += titles[titleIndex].charAt(charIndex);
        charIndex++;
        setTimeout(typeTitle, speed);
      } else {
        setTimeout(eraseTitle, 1500);
      }
    }

    function eraseTitle() {
      if (charIndex > 0) {
        target.textContent = titles[titleIndex].substring(0, charIndex - 1);
        charIndex--;
        setTimeout(eraseTitle, speed / 2);
      } else {
        titleIndex = (titleIndex + 1) % titles.length;
        setTimeout(typeTitle, speed);
      }
    }

    document.addEventListener("DOMContentLoaded", typeTitle);

    // Fade-in animation for testimonials
    const testimonialBoxes = document.querySelectorAll('.testimonial-box');

    window.addEventListener('scroll', () => {
      testimonialBoxes.forEach(box => {
        const rect = box.getBoundingClientRect();
        if (rect.top < window.innerHeight - 50) {
          box.classList.add('visible');
        }
      });
    });
  </script>
</body>
</html>
