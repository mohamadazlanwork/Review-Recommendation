<!-- 🌌 TESTIMONIALS SECTION -->
<section id="testimonials" style="position: relative; overflow: hidden; font-family: 'Poppins', sans-serif;">

  <!-- ✨ Animated Background -->
  <div class="background">
    <span></span><span></span><span></span><span></span><span></span>
    <span></span><span></span><span></span><span></span><span></span>
    <span></span><span></span><span></span><span></span><span></span>
    <span></span><span></span><span></span><span></span><span></span>
  </div>

  <!-- 🌟 Section Title -->
  <div class="testimonial-header">
    <h1>Professional Recommendations</h1>
    <p>Genuine words from learners and professionals who’ve experienced my support, mentorship, and dedication firsthand.</p>
  </div>

  <!-- 🟣 Google Reviews -->
  <div class="testimonial-section">
    <h3>🌟 Google Reviews</h3>
    <div class="testimonial-grid">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Averroes.png?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Aye%20-%20Learner.png?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Bryan.png?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Cho.png?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Hairul.png?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan/Htet.png?raw=true">
    </div>
  </div>

  <hr class="divider">

  <!-- 💼 LinkedIn Recommendations -->
  <div class="testimonial-section">
    <h3>💼 LinkedIn Recommendations</h3>
    <div class="testimonial-grid">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Syafiqah%201.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Fakhrul%20Azim%202.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aina%20Afiqah%203.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Yee%20Shai%204.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Anna%205.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Ying%20Shing%206.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Aliya%207.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Chee%20Low%208.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nurhuda%209.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/Nursyahirah%2010.jpg?raw=true">
      <img src="https://github.com/mohamadazlanwork/Powerbi_Dashboard/blob/main/Lithan%202%20Picture/last.jpg?raw=true">
    </div>
  </div>

  <blockquote class="testimonial-note">
    ⭐ All testimonials are authentic screenshots displayed for transparency — no edits or retyping were made.
  </blockquote>
</section>

<!-- 💫 STYLES -->
<style>
body {
  margin: 0;
  background: #3E1E68;
  overflow-x: hidden;
}

/* --- Header --- */
.testimonial-header {
  position: relative;
  text-align: center;
  color: #fff;
  padding: 80px 20px 40px;
  z-index: 2;
}
.testimonial-header h1 {
  font-size: 2.8em;
  letter-spacing: 1px;
  text-shadow: 0 2px 12px rgba(255,255,255,0.2);
}
.testimonial-header p {
  color: #ddd;
  max-width: 700px;
  margin: 10px auto;
  font-size: 1.1em;
}

/* --- Section Wrapper --- */
.testimonial-section {
  position: relative;
  background: rgba(255,255,255,0.05);
  padding: 40px;
  border-radius: 20px;
  margin: 0 auto 60px;
  max-width: 1200px;
  z-index: 2;
}
.testimonial-section h3 {
  text-align: center;
  font-size: 1.8em;
  color: #FFD580;
  margin-bottom: 20px;
}

/* --- Divider --- */
.divider {
  border: 0;
  border-top: 1px solid #f0cda6;
  margin: 40px auto;
  width: 80%;
  opacity: 0.6;
}

/* --- Grid Layout --- */
.testimonial-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
  justify-items: center;
  align-items: center;
}
.testimonial-grid img {
  width: 100%;
  max-width: 350px;
  border-radius: 12px;
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
  cursor: pointer;
  transform: perspective(600px) rotateX(0) rotateY(0);
}
.testimonial-grid img:hover {
  transform: scale(1.08) rotateX(6deg) rotateY(-6deg);
  box-shadow: 0 12px 35px rgba(255, 215, 150, 0.5);
}

/* --- Quote --- */
.testimonial-note {
  text-align: center;
  font-style: italic;
  color: #eee;
  margin: 40px auto;
  max-width: 800px;
  z-index: 2;
}

/* --- Animated Background --- */
.background {
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
  top: 0;
  left: 0;
  z-index: 0;
}
.background span {
  position: absolute;
  width: 20vmin;
  height: 20vmin;
  border-radius: 50%;
  background: radial-gradient(circle at center, rgba(255,255,255,0.3), transparent 70%);
  animation: move 10s linear infinite;
  opacity: 0.4;
}
@keyframes move {
  0% { transform: translateY(0) rotate(0deg) scale(1); }
  50% { transform: translateY(-20vh) rotate(180deg) scale(1.2); }
  100% { transform: translateY(0) rotate(360deg) scale(1); }
}
.background span:nth-child(odd) {
  background: radial-gradient(circle at center, #E45A84 30%, transparent 70%);
  animation-duration: 12s;
}
.background span:nth-child(even) {
  background: radial-gradient(circle at center, #FFACAC 30%, transparent 70%);
  animation-duration: 15s;
}
</style>
