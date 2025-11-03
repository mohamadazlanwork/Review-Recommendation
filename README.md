<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Azlan | Authentic Testimonials Gallery</title>

<!-- Google Fonts & Swiper -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.css" />

<style>
/* ===========================================================
   🎨 COLOR THEME — DARK ROYAL BLUE BEHANCE STYLE
   =========================================================== */
:root {
  --royal-blue: #0A1F44;
  --linkedin-blue: #0077B5;
  --deep-blue: #021024;
  --accent-cyan: #00FFFF;
  --accent-green: #34A853;
  --accent-yellow: #FBBC05;
  --accent-red: #EA4335;
  --glass-light: rgba(255,255,255,0.07);
  --glass-dark: rgba(0,0,0,0.3);
  --text-light: #E2E8F0;
  --text-dim: #94A3B8;
  --radius: 14px;
  --shadow-glow: 0 0 25px rgba(0,255,255,0.25);
}

/* ===========================================================
   🌌 GLOBAL LAYOUT + BACKGROUND
   =========================================================== */
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: radial-gradient(circle at top left, var(--royal-blue) 0%, var(--deep-blue) 100%);
  color: var(--text-light);
  overflow-x: hidden;
  transition: background 1s ease, color 0.8s ease;
  animation: backgroundFlow 20s infinite alternate ease-in-out;
}
@keyframes backgroundFlow {
  0% { background-position: 0% 50%; filter: brightness(1); }
  50% { background-position: 100% 50%; filter: brightness(1.1); }
  100% { background-position: 0% 50%; filter: brightness(1); }
}

/* Floating glow particles */
body::before {
  content: '';
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: radial-gradient(circle at 20% 30%, rgba(0,119,181,0.15), transparent 40%),
              radial-gradient(circle at 80% 70%, rgba(52,168,83,0.12), transparent 40%),
              radial-gradient(circle at 50% 90%, rgba(251,188,5,0.1), transparent 40%);
  z-index: 0;
  pointer-events: none;
  animation: particleGlow 40s linear infinite alternate;
}
@keyframes particleGlow {
  from { transform: translateY(0px); opacity: 0.8; }
  to { transform: translateY(-20px); opacity: 1; }
}

/* ===========================================================
   🧠 HEADER SECTION
   =========================================================== */
header {
  text-align: center;
  padding: 80px 20px 60px;
  position: relative;
  z-index: 2;
}
header h1 {
  font-size: 2.8em;
  font-weight: 700;
  background: linear-gradient(90deg, var(--accent-cyan), var(--linkedin-blue));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 0 0 18px rgba(0,255,255,0.3);
  animation: glowPulse 4s ease-in-out infinite alternate;
}
@keyframes glowPulse {
  0% { text-shadow: 0 0 15px rgba(0,255,255,0.2); }
  100% { text-shadow: 0 0 25px rgba(0,255,255,0.6); }
}
header p.subtitle {
  font-size: 1.1em;
  color: var(--text-dim);
  max-width: 800px;
  margin: 20px auto 0;
  line-height: 1.7;
}

/* ===========================================================
   🧭 TAB NAVIGATION
   =========================================================== */
.tabs {
  display: flex;
  justify-content: center;
  gap: 24px;
  margin: 50px 0 30px;
  z-index: 3;
  position: relative;
}
.tab-button {
  padding: 14px 32px;
  background: var(--glass-light);
  border: 1px solid rgba(255,255,255,0.2);
  border-radius: var(--radius);
  color: var(--text-light);
  font-size: 1.1em;
  font-weight: 600;
  letter-spacing: 0.5px;
  cursor: pointer;
  transition: all 0.4s ease;
  backdrop-filter: blur(10px);
}
.tab-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 0 18px rgba(0,255,255,0.25);
}
.tab-button.active {
  background: linear-gradient(135deg, var(--linkedin-blue), var(--accent-cyan));
  box-shadow: var(--shadow-glow);
  border-color: rgba(0,255,255,0.4);
}

/* ===========================================================
   🧊 CONTAINER
   =========================================================== */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px 100px;
  position: relative;
  z-index: 2;
}

/* ===========================================================
   🖼️ SWIPER BASE (for both sections)
   =========================================================== */
.swiper {
  width: 100%;
  padding-bottom: 60px;
}
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
}
.swiper-slide img {
  width: 100%;
  max-width: 380px;
  border-radius: var(--radius);
  box-shadow: 0 10px 25px rgba(0,0,0,0.4);
  transition: transform 0.5s ease, box-shadow 0.5s ease;
  cursor: pointer;
}
.swiper-slide img:hover {
  transform: scale(1.1) rotateY(6deg);
  box-shadow: 0 15px 40px rgba(0,255,255,0.3);
}

/* ===========================================================
   🪩 TRANSITION ANIMATIONS
   =========================================================== */
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 1.2s forwards;
}
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ===========================================================
   🧾 FOOTER BASE
   =========================================================== */
footer {
  text-align: center;
  font-size: 0.9em;
  color: var(--text-dim);
  padding: 40px 0 20px;
  border-top: 1px solid rgba(255,255,255,0.1);
  backdrop-filter: blur(6px);
}
footer span {
  color: var(--accent-cyan);
}

/* ===========================================================
   🔹 TAB CONTENT PLACEHOLDER
   =========================================================== */
.tab-content {
  display: none;
  opacity: 0;
  transition: opacity 1s ease;
}
.tab-content.active {
  display: block;
  opacity: 1;
}
</style>
</head>

<body>
  <div class="container fade-in">
    <header>
      <h1>Authentic Testimonials Gallery</h1>
      <p class="subtitle">
        Genuine appreciation and professional recommendations shared by <strong>learners and colleagues</strong> — showcasing trust, collaboration, and impact through real experiences.
      </p>
    </header>

    <div class="tabs">
      <button class="tab-button active" data-tab="google">🌈 Google Reviews</button>
      <button class="tab-button" data-tab="linkedin">💼 LinkedIn Recommendations</button>
    </div>
     <!-- ===========================================================
         🌈 GOOGLE REVIEWS SECTION (CINEMATIC STYLE)
         =========================================================== -->
    <div id="tab-google" class="tab-content active">
      <section id="google-section" style="
        background: linear-gradient(135deg, rgba(66,133,244,0.15), rgba(234,67,53,0.1));
        border-radius: 20px;
        box-shadow: 0 0 40px rgba(0,255,255,0.2);
        padding: 60px 25px;
        backdrop-filter: blur(14px);
      ">
        <h2 style="
          text-align:center;
          font-size:2em;
          font-weight:700;
          margin-bottom:45px;
          background:linear-gradient(90deg,#4285F4,#EA4335,#FBBC05,#34A853);
          -webkit-background-clip:text;
          -webkit-text-fill-color:transparent;
          animation:textShift 5s ease-in-out infinite alternate;
        ">🌟 Google Reviews</h2>

        <div class="swiper google-swiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Averroes.png?raw=true" alt="Averroes"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Aye%20-%20Learner.png?raw=true" alt="Aye"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Bryan.png?raw=true" alt="Bryan"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Cho.png?raw=true" alt="Cho"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Hairul.png?raw=true" alt="Hairul"></div>
            <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Htet.png?raw=true" alt="Htet"></div>
          </div>

          <div class="swiper-button-prev" style="color:#00FFFF;"></div>
          <div class="swiper-button-next" style="color:#00FFFF;"></div>
          <div class="swiper-pagination"></div>
        </div>

        <p style="
          text-align:center;
          margin-top:40px;
          font-style:italic;
          color:#a0aec0;
          font-size:0.95em;
          max-width:700px;
          margin-left:auto;
          margin-right:auto;
        ">
          ⭐ Authentic Google reviews from learners and colleagues who’ve experienced Azlan’s career support and mentorship.
        </p>
      </section>
    </div>

    <style>
      /* Smooth gradient pulse for text */
      @keyframes textShift {
        0% { text-shadow: 0 0 10px #4285F4; }
        50% { text-shadow: 0 0 14px #FBBC05; }
        100% { text-shadow: 0 0 12px #34A853; }
      }

      /* Hover glow */
      #google-section .swiper-slide img {
        border: 2px solid rgba(255,255,255,0.08);
        background: rgba(255,255,255,0.05);
        transition: transform 0.6s ease, box-shadow 0.6s ease;
      }
      #google-section .swiper-slide img:hover {
        transform: scale(1.08) rotateY(5deg);
        box-shadow: 0 20px 45px rgba(66,133,244,0.35);
      }

      /* Pagination dots styling */
      .google-swiper .swiper-pagination-bullet {
        background: #00FFFF;
        opacity: 0.6;
      }
      .google-swiper .swiper-pagination-bullet-active {
        background: #34A853;
        opacity: 1;
        box-shadow: 0 0 8px #00FFFF;
      }
    </style>
    <!-- ===========================================================
         💼 LINKEDIN RECOMMENDATIONS SECTION
         =========================================================== -->
    <div id="tab-linkedin" class="tab-content">
      <section id="linkedin-section" style="
        background: radial-gradient(circle at top, rgba(0,119,181,0.25), rgba(0,0,0,0.4));
        border-radius: 20px;
        padding: 60px 25px;
        box-shadow: 0 0 50px rgba(0,255,255,0.2);
        backdrop-filter: blur(18px);
      ">
        <h2 style="
          text-align:center;
          font-size:2em;
          font-weight:700;
          margin-bottom:45px;
          background:linear-gradient(90deg,#00A0DC,#0077B5,#00FFFF);
          -webkit-background-clip:text;
          -webkit-text-fill-color:transparent;
          text-shadow:0 0 20px rgba(0,255,255,0.4);
        ">💼 LinkedIn Recommendations</h2>

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

          <div class="swiper-button-prev" style="color:#00FFFF;"></div>
          <div class="swiper-button-next" style="color:#00FFFF;"></div>
          <div class="swiper-pagination"></div>
        </div>

        <p style="
          text-align:center;
          margin-top:40px;
          font-style:italic;
          color:#a0aec0;
          font-size:0.95em;
          max-width:700px;
          margin-left:auto;
          margin-right:auto;
        ">
          💬 Authentic LinkedIn recommendations from peers and professionals reflecting genuine collaboration and mentorship.
        </p>
      </section>
    </div>

    <!-- ===========================================================
         🔍 LIGHTBOX OVERLAY (BEHANCE STYLE)
         =========================================================== -->
    <div id="lightbox" style="
      display:none;
      position:fixed;
      top:0;left:0;width:100%;height:100%;
      background:rgba(0,0,0,0.9);
      justify-content:center;
      align-items:center;
      z-index:9999;
      backdrop-filter:blur(10px);
      transition:opacity 0.5s ease;
    ">
      <img id="lightbox-img" src="" alt="enlarged" style="
        max-width:90%;
        max-height:90%;
        border-radius:10px;
        box-shadow:0 0 40px rgba(0,255,255,0.5);
      "/>
      <span id="lightbox-close" style="
        position:absolute;top:40px;right:60px;
        color:#00FFFF;
        font-size:2em;
        cursor:pointer;
        font-weight:700;
      ">&times;</span>
    </div>

    <style>
      #linkedin-section .swiper-slide img {
        border: 2px solid rgba(255,255,255,0.1);
        background: rgba(255,255,255,0.03);
        transition: transform 0.6s ease, box-shadow 0.6s ease;
      }
      #linkedin-section .swiper-slide img:hover {
        transform: scale(1.08) rotateX(5deg);
        box-shadow: 0 20px 50px rgba(0,255,255,0.3);
      }
      .linkedin-swiper .swiper-pagination-bullet {
        background: #00FFFF;
        opacity: 0.5;
      }
      .linkedin-swiper .swiper-pagination-bullet-active {
        background: #0077B5;
        opacity: 1;
        box-shadow: 0 0 10px #00FFFF;
      }
    </style>

    <script>
      // Lightbox click-zoom
      const lightbox = document.getElementById('lightbox');
      const lightboxImg = document.getElementById('lightbox-img');
      const closeBtn = document.getElementById('lightbox-close');

      document.addEventListener('click', e => {
        if (e.target.tagName === 'IMG' && e.target.closest('.swiper-slide')) {
          lightbox.style.display = 'flex';
          lightboxImg.src = e.target.src;
        }
      });
      closeBtn.addEventListener('click', () => lightbox.style.display = 'none');
      lightbox.addEventListener('click', e => {
        if (e.target === lightbox) lightbox.style.display = 'none';
      });
    </script>
    <!-- ===========================================================
         ⚙️ SWIPER & TAB TRANSITIONS LOGIC
         =========================================================== -->
    <script src="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.js"></script>
    <script>
      // Google Reviews Swiper
      const googleSwiper = new Swiper('.google-swiper', {
        loop: true,
        autoplay: {
          delay: 3500,
          disableOnInteraction: false,
        },
        speed: 800,
        spaceBetween: 20,
        slidesPerView: 1,
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

      // LinkedIn Swiper (lazy init)
      let linkedinSwiper;
      let linkedinInitialized = false;

      function initLinkedInSwiper() {
        if (!linkedinInitialized) {
          linkedinSwiper = new Swiper('.linkedin-swiper', {
            loop: true,
            autoplay: {
              delay: 4000,
              disableOnInteraction: false,
            },
            speed: 900,
            spaceBetween: 25,
            slidesPerView: 1,
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
        }
      }

      // Tab switching logic
      const tabButtons = document.querySelectorAll('.tab-button');
      const tabContents = document.querySelectorAll('.tab-content');
      const body = document.body;

      tabButtons.forEach(btn => {
        btn.addEventListener('click', () => {
          const tab = btn.getAttribute('data-tab');
          tabButtons.forEach(b => b.classList.remove('active'));
          tabContents.forEach(c => c.classList.remove('active'));

          btn.classList.add('active');
          document.getElementById('tab-' + tab).classList.add('active');

          // Dynamic background transitions
          if (tab === 'google') {
            body.style.background =
              'radial-gradient(circle at top left, rgba(66,133,244,0.15), rgba(234,67,53,0.15)), linear-gradient(135deg,#0A1F44,#021024)';
          } else {
            body.style.background =
              'radial-gradient(circle at top, rgba(0,119,181,0.2), rgba(0,0,0,0.4)), linear-gradient(135deg,#00122B,#021024)';
            initLinkedInSwiper();
          }

          // smooth fade transition
          document.getElementById('tab-' + tab).classList.add('fade-in');
          setTimeout(() =>
            document.getElementById('tab-' + tab).classList.remove('fade-in'), 1200);
        });
      });

      // Handle autoplay pause/resume on hover
      document.querySelectorAll('.swiper').forEach(swiperEl => {
        swiperEl.addEventListener('mouseenter', () => {
          googleSwiper.autoplay.stop();
          if (linkedinSwiper) linkedinSwiper.autoplay.stop();
        });
        swiperEl.addEventListener('mouseleave', () => {
          googleSwiper.autoplay.start();
          if (linkedinSwiper) linkedinSwiper.autoplay.start();
        });
      });
    </script>

    <style>
      /* ===========================================================
         📱 RESPONSIVE BEHAVIOUR
         =========================================================== */
      @media (max-width: 768px) {
        header h1 { font-size: 2em; }
        header p.subtitle { font-size: 0.95em; }
        .tab-button { font-size: 1em; padding: 10px 20px; }
      }
      @media (max-width: 480px) {
        .tab-button { padding: 8px 16px; font-size: 0.9em; }
        .swiper-slide img { max-width: 280px; }
      }

      /* Fade overlay transition between tabs */
      .tab-content.fade-in {
        animation: softFade 1.1s ease forwards;
      }
      @keyframes softFade {
        from { opacity: 0; transform: scale(0.98); }
        to { opacity: 1; transform: scale(1); }
      }
    </style>
        <!-- ===========================================================
         🌠 FOOTER & AMBIENT EFFECTS
         =========================================================== -->
    <footer style="
      text-align:center;
      padding:40px 20px;
      color:#e0faff;
      font-size:0.95em;
      letter-spacing:0.5px;
      background:rgba(0,10,25,0.7);
      backdrop-filter:blur(10px);
      border-top:1px solid rgba(0,255,255,0.2);
      position:relative;
      overflow:hidden;
    ">
      <p style="
        margin:0;
        background:linear-gradient(90deg,#00A0DC,#00FFFF,#4285F4);
        -webkit-background-clip:text;
        -webkit-text-fill-color:transparent;
        animation:footerGlow 5s ease-in-out infinite alternate;
        font-weight:600;
      ">
        © 2025 Azlan | Testimonials Gallery – All Reviews Authentic & Publicly Available
      </p>
      <button id="scrollTop" style="
        position:absolute;right:30px;bottom:25px;
        background:linear-gradient(135deg,#0077B5,#00FFFF);
        color:white;border:none;
        border-radius:50%;width:42px;height:42px;
        font-size:20px;cursor:pointer;
        box-shadow:0 0 15px rgba(0,255,255,0.4);
        transition:all 0.4s ease;
      ">↑</button>
    </footer>

    <!-- Floating particles -->
    <canvas id="bgParticles" style="
      position:fixed;top:0;left:0;width:100%;height:100%;
      z-index:-1;pointer-events:none;
    "></canvas>

    <style>
      @keyframes footerGlow {
        0% { text-shadow:0 0 6px #00FFFF; }
        50% { text-shadow:0 0 14px #0077B5; }
        100% { text-shadow:0 0 10px #4285F4; }
      }
      #scrollTop:hover {
        transform:translateY(-4px);
        box-shadow:0 0 25px rgba(0,255,255,0.6);
      }
    </style>

    <script>
      // Smooth scroll-to-top
      const scrollBtn=document.getElementById('scrollTop');
      scrollBtn.addEventListener('click',()=>window.scrollTo({top:0,behavior:'smooth'}));

      // Floating particle background
      const canvas=document.getElementById('bgParticles');
      const ctx=canvas.getContext('2d');
      let w,h,particles=[];
      function resize(){w=canvas.width=window.innerWidth;h=canvas.height=window.innerHeight;}
      window.addEventListener('resize',resize);resize();
      for(let i=0;i<60;i++){
        particles.push({
          x:Math.random()*w,
          y:Math.random()*h,
          r:Math.random()*2+1,
          dx:(Math.random()-0.5)*0.5,
          dy:(Math.random()-0.5)*0.5,
          color:`hsl(${Math.random()*360},100%,70%)`
        });
      }
      function animate(){
        ctx.clearRect(0,0,w,h);
        particles.forEach(p=>{
          ctx.beginPath();
          ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
          ctx.fillStyle=p.color;
          ctx.fill();
          p.x+=p.dx;p.y+=p.dy;
          if(p.x<0||p.x>w)p.dx*=-1;
          if(p.y<0||p.y>h)p.dy*=-1;
        });
        requestAnimationFrame(animate);
      }
      animate();
    </script>


