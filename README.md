<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Landing Page</title>

  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #111, #333);
      color: #fff;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 60px 20px;
    }

    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.2em;
      color: #ccc;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 40px 20px;
    }

    .gallery img {
      width: 300px;
      height: 200px;
      object-fit: cover;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255, 0, 150, 0.5);
      transition: transform 0.4s ease, box-shadow 0.3s;
    }

    .gallery img:hover {
      transform: scale(1.08);
      box-shadow: 0 0 25px rgba(255, 0, 150, 0.8);
    }

    .features {
      max-width: 800px;
      margin: auto;
      text-align: center;
      padding: 40px 20px;
    }

    .features h2 {
      margin-bottom: 20px;
      color: #ff69b4;
    }

    .features ul {
      list-style: none;
      padding: 0;
    }

    .features li {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease;
      margin-bottom: 15px;
      font-size: 1.1em;
    }

    .features li.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .cta {
      text-align: center;
      margin: 50px 20px;
    }

    .cta a {
      display: inline-block;
      background-color: #ff007f;
      color: white;
      padding: 15px 35px;
      border-radius: 40px;
      font-size: 1.3em;
      text-decoration: none;
      transition: background-color 0.3s ease, transform 0.2s ease;
    }

    .cta a:hover {
      background-color: #ff3399;
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <header>
    <h1>Unlock Something Special</h1>
    <p>Premium visuals, secret content, and more – just one click away</p>
  </header>

  <div class="gallery">
    <img src="https://i.imgur.com/fHyEMsl.jpg" alt="Attractive Visual 1">
    <img src="https://i.imgur.com/8Km9tLL.jpg" alt="Attractive Visual 2">
    <img src="https://i.imgur.com/1c8ZQPp.jpg" alt="Attractive Visual 3">
  </div>

  <div class="features">
    <h2>Top Features</h2>
    <ul id="featureList">
      <li>Exclusive high-resolution galleries</li>
      <li>Fast-loading and mobile-friendly</li>
      <li>Hidden rewards and bonuses</li>
      <li>Daily updated surprises</li>
      <li>100% private and secure access</li>
    </ul>
  </div>

  <div class="cta">
    <a href="https://smrturl.co/a/scbbec0eb04/86?s1=" target="_blank">Click Here</a>
  </div>

  <script>
    // Reveal animation on scroll
    const features = document.querySelectorAll('#featureList li');

    function revealOnScroll() {
      const triggerBottom = window.innerHeight * 0.85;
      features.forEach(li => {
        const top = li.getBoundingClientRect().top;
        if (top < triggerBottom) {
          li.classList.add('visible');
        }
      });
    }

    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', revealOnScroll);
  </script>

</body>
</html>