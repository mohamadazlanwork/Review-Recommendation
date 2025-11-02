<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Testimonials – Tabbed Carousel</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.css" />
  <style>
    :root {
      --bg: #3E1E68;
      --text-light: #fff;
      --text-muted: #ddd;
      --accent: #E45A84;
      --accent2: #FFACAC;
      --section-bg: rgba(255, 255, 255, 0.05);
    }
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: var(--bg);
      color: var(--text-light);
      overflow-x: hidden;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 40px 20px;
    }
    .testimonial-header {
      text-align: center;
      padding: 60px 0 40px;
    }
    .testimonial-header h1 {
      font-size: 2.8em;
      text-shadow: 0 2px 12px rgba(255, 255, 255, 0.2);
      margin-bottom: 10px;
    }
    .testimonial-header p {
      color: var(--text-muted);
      font-size: 1.1em;
      max-width: 800px;
      margin: 0 auto;
    }
    .tabs {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 40px 0 20px;
    }
    .tab-button {
      padding: 12px 24px;
      background: var(--section-bg);
      border: none;
      border-radius: 8px;
      color: var(--text-light);
      cursor: pointer;
      font-size: 1.1em;
    }
    .tab-button.active {
      background: var(--accent);
      color: #fff;
    }
    .tab-content {
      display: none;
    }
    .tab-content.active {
      display: block;
    }
    .section-wrapper {
      background: var(--section-bg);
      padding: 40px 20px;
      border-radius: 20px;
      margin-bottom: 60px;
    }
    .section-wrapper h3 {
      text-align: center;
      font-size: 1.8em;
      margin-bottom: 20px;
      color: var(--accent2);
    }
    .swiper {
      width: 100%;
      padding-bottom: 40px;
    }
    .swiper-slide {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .swiper-slide img {
      width: 100%;
      max-width: 350px;
      border-radius: 12px;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
      transition: transform 0.4s, box-shadow 0.4s;
      cursor: pointer;
    }
    .swiper-slide img:hover {
      transform: scale(1.08) rotateX(6deg) rotateY(-6deg);
      box-shadow: 0 12px 35px rgba(255, 215, 150, 0.5);
    }
    .testimonial-note {
      text-align: center;
      font-style: italic;
      color: #eee;
      max-width: 800px;
      margin: 40px auto;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="testimonial-header">
      <h1>Professional Recommendations</h1>
      <p>Genuine words from learners and professionals who’ve experienced my support, mentorship, and dedication firsthand.</p>
    </div>

    <div class="tabs">
      <button class="tab-button active" data-tab="google">Google Reviews</button>
      <button class="tab-button" data-tab="linkedin">LinkedIn Recommendations</button>
    </div>

    <!-- Google Reviews Tab -->
    <div class="tab-content active" id="tab-google">
      <div class="section-wrapper">
        <h3>🌟 Google Reviews</h3>
        <div class="swiper google-swiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Averroes.png?raw=true" alt="Averroes"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Aye%20-%20Learner.png?raw=true" alt="Aye"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Bryan.png?raw=true" alt="Bryan"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Cho.png?raw=true" alt="Cho"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Hairul.png?raw=true" alt="Hairul"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Htet.png?raw=true" alt="Htet"></div>
          </div>
          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>
          <div class="swiper-pagination"></div>
        </div>
      </div>
    </div>

    <!-- LinkedIn Tab -->
    <div class="tab-content" id="tab-linkedin">
      <div class="section-wrapper">
        <h3>💼 LinkedIn Recommendations</h3>
        <div class="swiper linkedin-swiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Syafiqah%201.jpg?raw=true" alt="Syafiqah"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Fakhrul%20Azim%202.jpg?raw=true" alt="Fakhrul"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aina%20Afiqah%203.jpg?raw=true" alt="Aina"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Yee%20Shai%204.jpg?raw=true" alt="Yee Shai"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Anna%205.jpg?raw=true" alt="Anna"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Ying%20Shing%206.jpg?raw=true" alt="Ying"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aliya%207.jpg?raw=true" alt="Aliya"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Chee%20Low%208.jpg?raw=true" alt="Chee"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nurhuda%209.jpg?raw=true" alt="Nurhuda"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nursyahirah%2010.jpg?raw=true" alt="Syahirah"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/last.jpg?raw=true" alt="Final"></div>
          </div>
          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>
          <div class="swiper-pagination"></div>
        </div>
      </div>
    </div>

    <blockquote class="testimonial-note">
      ⭐ All testimonials are authentic screenshots displayed for transparency — no edits or retyping were made.
    </blockquote>
  </div>

  <!-- Swiper JS + Tab Logic -->
  <script src="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.js"></script>
  <script>
    const tabButtons = document.querySelectorAll('.tab-button');
    const tabContents = document.querySelectorAll('.tab-content');
    let linkedinInitialized = false;

    // Initialize Google Swiper
    const swiperGoogle = new Swiper('.google-swiper', {
      loop: true,
      slidesPerView: 1,
      spaceBetween: 20,
      navigation: {
        nextEl: '.google-swiper .swiper-button-next',
        prevEl: '.google-swiper .swiper-button-prev',
      },
      pagination: {
        el: '.google-swiper .swiper-pagination',
        clickable: true,
      },
      breakpoints: {
        768: { slidesPerView: 2 },
        1024: { slidesPerView: 3 }
      }
    });

    // Tab switching
    tabButtons.forEach(btn => {
      btn.addEventListener('click', () => {
        const tab = btn.getAttribute('data-tab');
        tabButtons.forEach(b => b.classList.remove('active'));
        tabContents.forEach(c => c.classList.remove('active'));
        btn.classList.add('active');
        document.getElementById('tab-' + tab).classList.add('active');

        if (tab === 'linkedin' && !linkedinInitialized) {
          setTimeout(() => {
            new Swiper('.linkedin-swiper', {
              loop: true,
              slidesPerView: 1,
              spaceBetween: 20,
              navigation: {
                nextEl: '.linkedin-swiper .swiper-button-next',
                prevEl: '.linkedin-swiper .swiper-button-prev',
              },
              pagination: {
                el: '.linkedin-swiper .swiper-pagination',
                clickable: true,
              },
              breakpoints: {
                768: { slidesPerView: 2 },
                1024: { slidesPerView: 3 }
              }
            });
            linkedinInitialized = true;
          }, 100);
        }
      });
    });
  </script>
</body>
</html>
