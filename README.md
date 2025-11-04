<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Azlan | Testimonials Gallery</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.css" />

<style>
:root{
  --dark-navy:#020617;
  --deep-space:#000814;
  --cyan:#00ffff;
  --teal:#00b8b8;
  --electric-blue:#009dff;
  --white:#f0faff;
  --glass-dark:rgba(255,255,255,0.05);
  --radius:18px;
}

/* ===== BODY ===== */
body{
  margin:0;
  font-family:'Poppins',sans-serif;
  background:radial-gradient(circle at top,#0d1b2a 0%,#000814 70%,#000 100%);
  color:var(--white);
  overflow-x:hidden;
  min-height:100vh;
  animation:bgShift 20s ease-in-out infinite alternate;
}
@keyframes bgShift{
  0%{background-position:0% 50%;}
  100%{background-position:100% 50%;}
}

/* Floating Glow */
body::before{
  content:"";
  position:fixed;inset:0;
  background:
    radial-gradient(circle at 20% 30%,rgba(0,255,255,0.15),transparent 40%),
    radial-gradient(circle at 80% 70%,rgba(0,157,255,0.15),transparent 40%);
  pointer-events:none;
  animation:floatGlow 30s linear infinite alternate;
  z-index:0;
}
@keyframes floatGlow{
  from{transform:translateY(0);}
  to{transform:translateY(-30px);}
}

/* ===========================================================
   HEADER
   =========================================================== */
header{
  text-align:center;
  padding:80px 20px 50px;
  z-index:2;
  position:relative;
}
header h1{
  font-size:2.8em;
  font-weight:700;
  background:linear-gradient(90deg,var(--teal),var(--cyan));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  text-shadow:0 0 25px rgba(0,255,255,0.5);
}
header p{
  color:#cbd5e1;
  font-size:1.1em;
  max-width:700px;
  margin:15px auto 0;
  line-height:1.6;
}

/* ===========================================================
   TABS
   =========================================================== */
.tabs{
  display:flex;
  justify-content:center;
  gap:20px;
  flex-wrap:wrap;
  margin:40px 0 60px;
  z-index:2;
  position:relative;
}
.tab-button{
  padding:12px 32px;
  border:1px solid rgba(0,255,255,0.4);
  border-radius:var(--radius);
  color:var(--white);
  background:var(--glass-dark);
  backdrop-filter:blur(8px);
  font-weight:600;
  letter-spacing:0.5px;
  cursor:pointer;
  transition:all 0.4s ease;
  box-shadow:0 0 15px rgba(0,255,255,0.1);
}
.tab-button:hover{
  transform:translateY(-3px);
  box-shadow:0 0 20px rgba(0,255,255,0.4);
}
.tab-button.active{
  background:linear-gradient(135deg,var(--teal),var(--electric-blue));
  box-shadow:0 0 25px rgba(0,255,255,0.5);
}

/* ===========================================================
   SWIPER
   =========================================================== */
.swiper{width:100%;padding-bottom:60px;}
.swiper-slide{display:flex;justify-content:center;align-items:center;}
.swiper-slide img{
  width:100%;max-width:380px;border-radius:var(--radius);
  box-shadow:0 8px 25px rgba(0,255,255,0.1);
  transition:transform 0.6s ease,box-shadow 0.6s ease;
  cursor:pointer;
}
.swiper-slide img:hover{
  transform:scale(1.08) rotateY(6deg);
  box-shadow:0 0 45px rgba(0,255,255,0.5);
}

/* ===========================================================
   TAB CONTENT CONTAINERS
   =========================================================== */
.container{max-width:1200px;margin:auto;padding:0 20px 100px;position:relative;z-index:1;}
.tab-content{display:none;opacity:0;transition:opacity 0.6s ease;}
.tab-content.active{display:block;opacity:1;}
.section{
  background:rgba(255,255,255,0.03);
  border:1px solid rgba(0,255,255,0.1);
  border-radius:var(--radius);
  padding:60px 25px;
  backdrop-filter:blur(12px);
  box-shadow:inset 0 0 30px rgba(0,255,255,0.05),0 0 40px rgba(0,255,255,0.1);
}

/* ===========================================================
   LIGHTBOX
   =========================================================== */
#lightbox{
  display:none;position:fixed;top:0;left:0;width:100%;height:100%;
  background:rgba(0,0,0,0.95);
  justify-content:center;align-items:center;
  z-index:9999;backdrop-filter:blur(8px);
}
#lightbox img{
  max-width:90%;max-height:90%;border-radius:10px;
  box-shadow:0 0 45px rgba(0,255,255,0.6);
}
#lightbox-close{
  position:absolute;top:40px;right:60px;
  color:var(--cyan);font-size:2em;cursor:pointer;font-weight:700;
}

/* ===========================================================
   FOOTER + SCROLL BUTTON
   =========================================================== */
footer{
  text-align:center;
  padding:50px 20px 30px;
  color:#a0f0ff;
  font-weight:600;
  border-top:1px solid rgba(0,255,255,0.2);
  background:rgba(255,255,255,0.02);
  backdrop-filter:blur(8px);
}
#scrollTop{
  position:fixed;
  bottom:30px;right:30px;
  width:45px;height:45px;
  border:none;border-radius:50%;
  background:linear-gradient(135deg,var(--cyan),var(--electric-blue));
  color:#000;font-size:18px;font-weight:bold;
  cursor:pointer;
  box-shadow:0 0 20px rgba(0,255,255,0.4);
  transition:all 0.4s ease;
}
#scrollTop:hover{transform:translateY(-4px);box-shadow:0 0 35px rgba(0,255,255,0.7);}

/* ===========================================================
   PARTICLES CANVAS
   =========================================================== */
#bgParticles{position:fixed;top:0;left:0;width:100%;height:100%;z-index:-1;pointer-events:none;}
</style>
</head>
<body>

<canvas id="bgParticles"></canvas>

<div class="container">
  <header>
    <h1>Google Reviews & LinkedIn Recommendations</h1>
    <p>True appreciation and recommendations from <strong>learners and colleagues</strong>.</p>
  </header>

  <div class="tabs">
    <button class="tab-button active" data-tab="google">🌌 Google Reviews</button>
    <button class="tab-button" data-tab="linkedin">💠 LinkedIn Recommendations</button>
  </div>

  <!-- GOOGLE REVIEWS -->
  <div id="tab-google" class="tab-content active">
    <section class="section">
      <h2 style="text-align:center;color:var(--cyan);">🌟 Google Reviews</h2>
      <div class="swiper google-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Averroes.png?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Aye%20-%20Learner.png?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Bryan.png?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Cho.png?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Hairul.png?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Htet.png?raw=true"></div>
        </div>
        <div class="swiper-pagination"></div>
      </div>
    </section>
  </div>

  <!-- LINKEDIN RECOMMENDATIONS -->
  <div id="tab-linkedin" class="tab-content">
    <section class="section">
      <h2 style="text-align:center;color:var(--cyan);">💼 LinkedIn Recommendations</h2>
      <div class="swiper linkedin-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Syafiqah%201.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Fakhrul%20Azim%202.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aina%20Afiqah%203.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Yee%20Shai%204.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Anna%205.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Ying%20Shing%206.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aliya%207.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Chee%20Low%208.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nurhuda%209.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nursyahirah%2010.jpg?raw=true"></div>
          <div class="swiper-slide"><img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/last.jpg?raw=true"></div>
        </div>
        <div class="swiper-pagination"></div>
      </div>
    </section>
  </div>
</div>

<footer>© 2025 Azlan | All Reviews Verified</footer>
<button id="scrollTop">↑</button>

<!-- LIGHTBOX -->
<div id="lightbox">
  <img id="lightbox-img" src="" alt="enlarged">
  <span id="lightbox-close">&times;</span>
</div>

<script src="https://cdn.jsdelivr.net/npm/swiper@12/swiper-bundle.min.js"></script>
<script>
// Swipers
const googleSwiper=new Swiper('.google-swiper',{loop:true,autoplay:{delay:3000,disableOnInteraction:false},
slidesPerView:1,spaceBetween:15,pagination:{el:'.google-swiper .swiper-pagination',clickable:true},
breakpoints:{768:{slidesPerView:2},1024:{slidesPerView:3}}});
let linkedinSwiper;
function initLinkedInSwiper(){
  if(!linkedinSwiper){
    linkedinSwiper=new Swiper('.linkedin-swiper',{loop:true,autoplay:{delay:3500,disableOnInteraction:false},
    slidesPerView:1,spaceBetween:15,pagination:{el:'.linkedin-swiper .swiper-pagination',clickable:true},
    breakpoints:{768:{slidesPerView:2},1024:{slidesPerView:3}}});
  }
}
// Tabs
document.querySelectorAll('.tab-button').forEach(btn=>{
  btn.addEventListener('click',()=>{
    document.querySelectorAll('.tab-button').forEach(b=>b.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(c=>c.classList.remove('active'));
    btn.classList.add('active');
    const tab=btn.dataset.tab;
    document.getElementById('tab-'+tab).classList.add('active');
    if(tab==='linkedin')initLinkedInSwiper();
  });
});
// Lightbox
const lb=document.getElementById('lightbox');
const lbImg=document.getElementById('lightbox-img');
document.addEventListener('click',e=>{
  if(e.target.tagName==='IMG'&&e.target.closest('.swiper-slide')){lb.style.display='flex';lbImg.src=e.target.src;}
});
document.getElementById('lightbox-close').onclick=()=>lb.style.display='none';
lb.onclick=e=>{if(e.target===lb)lb.style.display='none';};
// Scroll
document.getElementById('scrollTop').onclick=()=>window.scrollTo({top:0,behavior:'smooth'});
// Particles
const c=document.getElementById('bgParticles');const ctx=c.getContext('2d');let w,h,particles=[];
function resize(){w=c.width=window.innerWidth;h=c.height=window.innerHeight;}
window.addEventListener('resize',resize);resize();
for(let i=0;i<80;i++){particles.push({x:Math.random()*w,y:Math.random()*h,r:Math.random()*2+1,dx:(Math.random()-0.5)*0.8,dy:(Math.random()-0.5)*0.8,color:`hsl(${Math.random()*180+160},100%,60%)`});}
function animate(){
  ctx.clearRect(0,0,w,h);
  particles.forEach(p=>{
    ctx.beginPath();ctx.arc(p.x,p.y,p.r,0,Math.PI*2);
    ctx.fillStyle=p.color;ctx.fill();
    p.x+=p.dx;p.y+=p.dy;
    if(p.x<0||p.x>w)p.dx*=-1;
    if(p.y<0||p.y>h)p.dy*=-1;
  });
  requestAnimationFrame(animate);
}
animate();
</script>
</body>
</html>
