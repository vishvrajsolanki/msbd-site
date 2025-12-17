<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MSBD Scroll Animation</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    body {
      background: #0f172a;
      color: #e5e7eb;
    }

    header {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      background: linear-gradient(135deg, #2563eb, #1e40af);
    }

    section {
      min-height: 100vh;
      padding: 80px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.6rem;

      opacity: 0;
      transform: translateY(60px);
      transition: all 0.8s ease;
    }

    section:nth-child(even) {
      background: #020617;
    }

    section:nth-child(odd) {
      background: #020617;
    }

    footer {
      padding: 40px;
      text-align: center;
      background: #020617;
      font-size: 1rem;
    }
  </style>
</head>
<body>

  <header>
    <div>Welcome to MSBD</div>
  </header>

  <section class="animate">
    <div>Section 1 – Scroll Down</div>
  </section>

  <section class="animate">
    <div>Section 2 – Smooth Animation</div>
  </section>

  <section class="animate">
    <div>Section 3 – Modern Effect</div>
  </section>

  <footer>
    © 2025 MSBD Project
  </footer>

  <script>
    const observerOptions = {
      threshold: 0.2
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, observerOptions);

    document.querySelectorAll('.animate').forEach(section => {
      observer.observe(section);
    });
  </script>

</body>
</html>
