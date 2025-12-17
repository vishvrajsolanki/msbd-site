<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Mahi</title>

    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: #ffffff;
            scroll-behavior: smooth;
        }

        section {
            min-height: 100vh;
            padding: 60px 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .container {
            max-width: 900px;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        h2 {
            font-size: 2.2rem;
            margin-bottom: 15px;
        }

        p {
            font-size: 1.1rem;
            line-height: 1.8;
            opacity: 0.9;
        }

        .hero {
            background: rgba(0,0,0,0.3);
        }

        .friendship,
        .wishes,
        .surprise {
            background: rgba(255,255,255,0.05);
        }

        .card {
            background: rgba(0,0,0,0.4);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.4);
        }

        .footer {
            background: rgba(0,0,0,0.6);
            padding: 40px 20px;
        }

        .footer p {
            font-size: 0.95rem;
            opacity: 0.8;
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 2.2rem;
            }
            h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>

    <!-- HERO -->
    <section class="hero">
        <div class="container">
            <h1>Happy Birthday Mahi</h1>
            <p>
                Today is a special day, and this small website is just a simple way
                to wish you happiness, success, and a bright future.
            </p>
        </div>
    </section>

    <!-- FRIENDSHIP -->
    <section class="friendship">
        <div class="container card">
            <h2>About Our Friendship</h2>
            <p>
                Mahi, you are my first and best friend.
                Friendship like ours is not about talking every day,
                but about understanding, trust, and respect.
                I truly value this bond and always will.
            </p>
        </div>
    </section>

    <!-- WISHES -->
    <section class="wishes">
        <div class="container card">
            <h2>Birthday Wishes</h2>
            <p>
                May this new year of your life bring confidence,
                positivity, and opportunities.
                May you achieve everything you truly deserve.
                Keep smiling and moving forward.
            </p>
        </div>
    </section>

    <!-- SURPRISE -->
    <section class="surprise">
        <div class="container card">
            <h2>A Small Message</h2>
            <p>
                If you ever need help or support in life,
                remember that I am always here.
                This website is simple, but the wish behind it is genuine.
            </p>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
        <div class="container">
            <p>
                Made with sincerity and respect <br>
                From Vishvraj
            </p>
        </div>
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

        document.querySelectorAll(
            '.friendship, .wishes, .surprise, .footer'
        ).forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 1s ease, transform 1s ease';
            observer.observe(section);
        });
    </script>

</body>
</html>
