<script setup>
import Topic from './components/Topic.vue'
import Info from './components/Info.vue'
import Tips from './components/Tips.vue'
</script>

<template>
  <div id="app">
    <div class="ocean-scene">
      <div class="ocean-gradient"></div>
      
      <!-- Realistic water surface with SVG waves -->
      <div class="water-surface">
        <svg class="water-wave" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" preserveAspectRatio="none">
          <path class="wave-path wave-1" d="M0,160L48,176C96,192,192,224,288,224C384,224,480,192,576,165.3C672,139,768,117,864,128C960,139,1056,181,1152,186.7C1248,192,1344,160,1392,144L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z" fill="rgba(46, 185, 209, 0.3)"></path>
        </svg>
        <svg class="water-wave" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" preserveAspectRatio="none">
          <path class="wave-path wave-2" d="M0,96L48,112C96,128,192,160,288,165.3C384,171,480,149,576,154.7C672,160,768,192,864,197.3C960,203,1056,181,1152,165.3C1248,149,1344,139,1392,133.3L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z" fill="rgba(102, 217, 232, 0.2)"></path>
        </svg>
        <svg class="water-wave" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" preserveAspectRatio="none">
          <path class="wave-path wave-3" d="M0,224L48,213.3C96,203,192,181,288,181.3C384,181,480,203,576,213.3C672,224,768,224,864,208C960,192,1056,160,1152,154.7C1248,149,1344,171,1392,181.3L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z" fill="rgba(92, 225, 230, 0.15)"></path>
        </svg>
      </div>

      <!-- Rising bubbles for underwater effect -->
      <div class="bubbles">
        <div class="bubble" v-for="n in 20" :key="'bubble-' + n"></div>
      </div>

      <!-- Water light rays -->
      <div class="light-rays">
        <div class="light-ray" v-for="n in 5" :key="'ray-' + n"></div>
      </div>

      <!-- Floating microplastic particles -->
      <div class="particles">
        <div class="particle" v-for="n in 40" :key="n"></div>
      </div>

      <!-- Water shimmer effect -->
      <div class="water-shimmer"></div>

      <!-- Swimming Fish -->
      <div class="fish-container">
        <div class="fish" v-for="n in 8" :key="'fish-' + n"></div>
      </div>
    </div>

    <div class="container">
      <header class="hero-section">
        <div class="hero-badge">
          <span class="badge-text">Environmental Awareness</span>
        </div>
        <h1 class="hero-title">
          Microplastic<br/>
          <span class="highlight">Pollution Crisis</span>
        </h1>
        <p class="hero-subtitle">
          Understanding the invisible threat to our oceans, wildlife, and health
        </p>
        
        <div class="stats-row">
          <div class="stat-item">
            <div class="stat-number">5mm</div>
            <div class="stat-label">Maximum Size</div>
          </div>
          <div class="stat-divider"></div>
          <div class="stat-item">
            <div class="stat-number">5 Trillion</div>
            <div class="stat-label">Particles in Oceans</div>
          </div>
          <div class="stat-divider"></div>
          <div class="stat-item">
            <div class="stat-number">100+</div>
            <div class="stat-label">Years to Decompose</div>
          </div>
        </div>
      </header>

      <Topic />
      <Info />
      <Tips />

     
      <footer class="site-footer">
        <p>🌍 Together, we can protect our oceans and planet</p>
        <p class="footer-credit">Environmental Awareness Project © 2026</p>
      </footer>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700;800;900&family=Manrope:wght@400;500;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --ocean-deepest: #0a2342;
  --ocean-deep: #0f4c75;
  --ocean-mid: #1891ac;
  --ocean-bright: #2eb9d1;
  --ocean-foam: #66d9e8;
  --coral: #ff6b6b;
  --coral-light: #ff8787;
  --sand: #f4e8d8;
  --sand-dark: #e6d5c3;
  --white: #ffffff;
  --text-primary: #1a2332;
  --text-secondary: #4a5568;
  --text-light: #718096;
}

body {
  font-family: 'Manrope', -apple-system, BlinkMacSystemFont, sans-serif;
  color: var(--text-primary);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
  background: var(--ocean-deepest);
}

#app {
  position: relative;
  min-height: 100vh;
}

.ocean-scene {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  z-index: 0;
  overflow: hidden;
}

.ocean-gradient {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    180deg,
    var(--ocean-deepest) 0%,
    var(--ocean-deep) 30%,
    var(--ocean-mid) 60%,
    var(--ocean-bright) 100%
  );
}

/* Realistic SVG Water Waves */
.water-surface {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 400px;
  overflow: hidden;
}

.water-wave {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.wave-path {
  animation: wave-motion 8s ease-in-out infinite;
}

.wave-1 {
  animation-delay: 0s;
  animation-duration: 10s;
}

.wave-2 {
  animation-delay: -2s;
  animation-duration: 12s;
}

.wave-3 {
  animation-delay: -4s;
  animation-duration: 14s;
}

@keyframes wave-motion {
  0%, 100% {
    transform: translateX(0) translateY(0);
  }
  25% {
    transform: translateX(-5%) translateY(-10px);
  }
  50% {
    transform: translateX(-10%) translateY(0);
  }
  75% {
    transform: translateX(-5%) translateY(10px);
  }
}

/* Rising Bubbles - Underwater Effect */
.bubbles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.bubble {
  position: absolute;
  bottom: -100px;
  background: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.3));
  border-radius: 50%;
  opacity: 0;
  animation: rise 15s infinite ease-in;
  box-shadow: 
    inset 0 0 10px rgba(255, 255, 255, 0.5),
    0 0 10px rgba(102, 217, 232, 0.3);
}

.bubble:nth-child(1) { left: 10%; width: 40px; height: 40px; animation-delay: 0s; animation-duration: 12s; }
.bubble:nth-child(2) { left: 20%; width: 30px; height: 30px; animation-delay: 2s; animation-duration: 14s; }
.bubble:nth-child(3) { left: 30%; width: 50px; height: 50px; animation-delay: 4s; animation-duration: 16s; }
.bubble:nth-child(4) { left: 40%; width: 35px; height: 35px; animation-delay: 1s; animation-duration: 13s; }
.bubble:nth-child(5) { left: 50%; width: 45px; height: 45px; animation-delay: 3s; animation-duration: 15s; }
.bubble:nth-child(6) { left: 60%; width: 25px; height: 25px; animation-delay: 5s; animation-duration: 11s; }
.bubble:nth-child(7) { left: 70%; width: 55px; height: 55px; animation-delay: 2s; animation-duration: 17s; }
.bubble:nth-child(8) { left: 80%; width: 30px; height: 30px; animation-delay: 4s; animation-duration: 12s; }
.bubble:nth-child(9) { left: 90%; width: 40px; height: 40px; animation-delay: 1s; animation-duration: 14s; }
.bubble:nth-child(10) { left: 15%; width: 35px; height: 35px; animation-delay: 3s; animation-duration: 16s; }
.bubble:nth-child(11) { left: 25%; width: 45px; height: 45px; animation-delay: 0s; animation-duration: 13s; }
.bubble:nth-child(12) { left: 35%; width: 28px; height: 28px; animation-delay: 5s; animation-duration: 15s; }
.bubble:nth-child(13) { left: 45%; width: 50px; height: 50px; animation-delay: 2s; animation-duration: 11s; }
.bubble:nth-child(14) { left: 55%; width: 32px; height: 32px; animation-delay: 4s; animation-duration: 17s; }
.bubble:nth-child(15) { left: 65%; width: 42px; height: 42px; animation-delay: 1s; animation-duration: 12s; }
.bubble:nth-child(16) { left: 75%; width: 38px; height: 38px; animation-delay: 3s; animation-duration: 14s; }
.bubble:nth-child(17) { left: 85%; width: 48px; height: 48px; animation-delay: 0s; animation-duration: 16s; }
.bubble:nth-child(18) { left: 95%; width: 26px; height: 26px; animation-delay: 5s; animation-duration: 13s; }
.bubble:nth-child(19) { left: 12%; width: 36px; height: 36px; animation-delay: 2s; animation-duration: 15s; }
.bubble:nth-child(20) { left: 88%; width: 44px; height: 44px; animation-delay: 4s; animation-duration: 11s; }

@keyframes rise {
  0% {
    bottom: -100px;
    opacity: 0;
    transform: translateX(0) scale(1);
  }
  10% {
    opacity: 1;
  }
  50% {
    transform: translateX(20px) scale(1.1);
  }
  90% {
    opacity: 0.8;
  }
  100% {
    bottom: 110%;
    opacity: 0;
    transform: translateX(-20px) scale(0.8);
  }
}

/* Underwater Light Rays */
.light-rays {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.light-ray {
  position: absolute;
  top: -10%;
  width: 100px;
  height: 120%;
  background: linear-gradient(
    to bottom,
    rgba(255, 255, 255, 0.15) 0%,
    rgba(255, 255, 255, 0.08) 30%,
    transparent 70%
  );
  transform-origin: top center;
  animation: sway-light 10s ease-in-out infinite;
  opacity: 0.6;
}

.light-ray:nth-child(1) {
  left: 10%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.light-ray:nth-child(2) {
  left: 30%;
  animation-delay: -2s;
  animation-duration: 14s;
}

.light-ray:nth-child(3) {
  left: 50%;
  animation-delay: -4s;
  animation-duration: 16s;
}

.light-ray:nth-child(4) {
  left: 70%;
  animation-delay: -1s;
  animation-duration: 13s;
}

.light-ray:nth-child(5) {
  left: 90%;
  animation-delay: -3s;
  animation-duration: 15s;
}

@keyframes sway-light {
  0%, 100% {
    transform: rotate(-2deg);
    opacity: 0.4;
  }
  50% {
    transform: rotate(2deg);
    opacity: 0.7;
  }
}

.particles {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: rgba(255, 255, 255, 0.6);
  border-radius: 50%;
  animation: float-particle 20s infinite ease-in-out;
}

.particle:nth-child(odd) {
  background: rgba(102, 217, 232, 0.5);
}

.particle:nth-child(1) { left: 10%; top: 20%; animation-delay: 0s; animation-duration: 15s; }
.particle:nth-child(2) { left: 20%; top: 60%; animation-delay: 2s; animation-duration: 18s; }
.particle:nth-child(3) { left: 30%; top: 40%; animation-delay: 4s; animation-duration: 22s; }
.particle:nth-child(4) { left: 40%; top: 80%; animation-delay: 1s; animation-duration: 20s; }
.particle:nth-child(5) { left: 50%; top: 30%; animation-delay: 3s; animation-duration: 16s; }
.particle:nth-child(6) { left: 60%; top: 70%; animation-delay: 5s; animation-duration: 19s; }
.particle:nth-child(7) { left: 70%; top: 50%; animation-delay: 2s; animation-duration: 21s; }
.particle:nth-child(8) { left: 80%; top: 25%; animation-delay: 4s; animation-duration: 17s; }
.particle:nth-child(9) { left: 90%; top: 65%; animation-delay: 1s; animation-duration: 23s; }
.particle:nth-child(10) { left: 15%; top: 45%; animation-delay: 3s; animation-duration: 18s; }
.particle:nth-child(11) { left: 25%; top: 85%; animation-delay: 0s; animation-duration: 20s; }
.particle:nth-child(12) { left: 35%; top: 15%; animation-delay: 5s; animation-duration: 16s; }
.particle:nth-child(13) { left: 45%; top: 55%; animation-delay: 2s; animation-duration: 22s; }
.particle:nth-child(14) { left: 55%; top: 35%; animation-delay: 4s; animation-duration: 19s; }
.particle:nth-child(15) { left: 65%; top: 75%; animation-delay: 1s; animation-duration: 21s; }
.particle:nth-child(16) { left: 75%; top: 20%; animation-delay: 3s; animation-duration: 17s; }
.particle:nth-child(17) { left: 85%; top: 60%; animation-delay: 0s; animation-duration: 23s; }
.particle:nth-child(18) { left: 95%; top: 40%; animation-delay: 5s; animation-duration: 18s; }
.particle:nth-child(19) { left: 12%; top: 70%; animation-delay: 2s; animation-duration: 20s; }
.particle:nth-child(20) { left: 22%; top: 10%; animation-delay: 4s; animation-duration: 16s; }
.particle:nth-child(21) { left: 32%; top: 90%; animation-delay: 1s; animation-duration: 22s; }
.particle:nth-child(22) { left: 42%; top: 50%; animation-delay: 3s; animation-duration: 19s; }
.particle:nth-child(23) { left: 52%; top: 30%; animation-delay: 0s; animation-duration: 21s; }
.particle:nth-child(24) { left: 62%; top: 80%; animation-delay: 5s; animation-duration: 17s; }
.particle:nth-child(25) { left: 72%; top: 45%; animation-delay: 2s; animation-duration: 23s; }
.particle:nth-child(26) { left: 82%; top: 15%; animation-delay: 4s; animation-duration: 18s; }
.particle:nth-child(27) { left: 92%; top: 75%; animation-delay: 1s; animation-duration: 20s; }
.particle:nth-child(28) { left: 18%; top: 55%; animation-delay: 3s; animation-duration: 16s; }
.particle:nth-child(29) { left: 28%; top: 25%; animation-delay: 0s; animation-duration: 22s; }
.particle:nth-child(30) { left: 38%; top: 65%; animation-delay: 5s; animation-duration: 19s; }

@keyframes float-particle {
  0%, 100% {
    transform: translateY(0) translateX(0);
    opacity: 0;
  }
  10% {
    opacity: 0.8;
  }
  90% {
    opacity: 0.8;
  }
  50% {
    transform: translateY(-100px) translateX(50px);
    opacity: 1;
  }
}

/* Water Shimmer/Reflection Effect */
.water-shimmer {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    radial-gradient(ellipse at 20% 30%, rgba(255, 255, 255, 0.1) 0%, transparent 40%),
    radial-gradient(ellipse at 80% 60%, rgba(255, 255, 255, 0.08) 0%, transparent 40%),
    radial-gradient(ellipse at 40% 80%, rgba(255, 255, 255, 0.06) 0%, transparent 40%);
  animation: shimmer 8s ease-in-out infinite;
  pointer-events: none;
}

@keyframes shimmer {
  0%, 100% {
    opacity: 0.5;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.1);
  }
}

/* Swimming Fish */
.fish-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.fish {
  position: absolute;
  width: 40px;
  height: 20px;
  background: linear-gradient(135deg, rgba(255, 165, 0, 0.8), rgba(255, 200, 100, 0.9));
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
  animation: swim 15s infinite linear;
  opacity: 0.8;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
}

.fish::before {
  content: '';
  position: absolute;
  right: -10px;
  top: 50%;
  transform: translateY(-50%);
  width: 0;
  height: 0;
  border-left: 15px solid rgba(255, 165, 0, 0.8);
  border-top: 8px solid transparent;
  border-bottom: 8px solid transparent;
}

.fish::after {
  content: '';
  position: absolute;
  left: 8px;
  top: 6px;
  width: 4px;
  height: 4px;
  background: rgba(0, 0, 0, 0.8);
  border-radius: 50%;
}

.fish:nth-child(1) { 
  top: 15%; 
  width: 50px; 
  height: 25px; 
  animation-duration: 20s; 
  animation-delay: 0s;
  background: linear-gradient(135deg, rgba(46, 185, 209, 0.9), rgba(102, 217, 232, 0.9));
}

.fish:nth-child(1)::before { 
  border-left-color: rgba(46, 185, 209, 0.9); 
}

.fish:nth-child(2) { 
  top: 30%; 
  width: 35px; 
  height: 18px; 
  animation-duration: 25s; 
  animation-delay: -5s;
  background: linear-gradient(135deg, rgba(255, 107, 107, 0.8), rgba(255, 135, 135, 0.9));
}

.fish:nth-child(2)::before { 
  border-left-color: rgba(255, 107, 107, 0.8); 
}

.fish:nth-child(3) { 
  top: 50%; 
  width: 45px; 
  height: 22px; 
  animation-duration: 18s; 
  animation-delay: -10s;
  background: linear-gradient(135deg, rgba(102, 217, 168, 0.9), rgba(126, 229, 184, 0.9));
}

.fish:nth-child(3)::before { 
  border-left-color: rgba(102, 217, 168, 0.9); 
}

.fish:nth-child(4) { 
  top: 65%; 
  width: 30px; 
  height: 15px; 
  animation-duration: 22s; 
  animation-delay: -15s;
  background: linear-gradient(135deg, rgba(155, 89, 182, 0.8), rgba(192, 152, 219, 0.9));
}

.fish:nth-child(4)::before { 
  border-left-color: rgba(155, 89, 182, 0.8); 
}

.fish:nth-child(5) { 
  top: 25%; 
  width: 55px; 
  height: 28px; 
  animation-duration: 28s; 
  animation-delay: -8s;
  animation-direction: reverse;
  background: linear-gradient(135deg, rgba(241, 196, 15, 0.8), rgba(243, 213, 91, 0.9));
}

.fish:nth-child(5)::before { 
  border-left-color: rgba(241, 196, 15, 0.8); 
  right: auto;
  left: -10px;
  border-left: none;
  border-right: 15px solid rgba(241, 196, 15, 0.8);
}

.fish:nth-child(6) { 
  top: 45%; 
  width: 38px; 
  height: 19px; 
  animation-duration: 24s; 
  animation-delay: -12s;
  background: linear-gradient(135deg, rgba(52, 152, 219, 0.8), rgba(93, 173, 226, 0.9));
}

.fish:nth-child(6)::before { 
  border-left-color: rgba(52, 152, 219, 0.8); 
}

.fish:nth-child(7) { 
  top: 70%; 
  width: 42px; 
  height: 21px; 
  animation-duration: 19s; 
  animation-delay: -18s;
  animation-direction: reverse;
  background: linear-gradient(135deg, rgba(230, 126, 34, 0.8), rgba(235, 152, 78, 0.9));
}

.fish:nth-child(7)::before { 
  border-left-color: rgba(189, 162, 138, 0.8); 
  right: auto;
  left: -10px;
  border-left: none;
  border-right: 15px solid rgba(230, 126, 34, 0.8);
}

.fish:nth-child(8) { 
  top: 55%; 
  width: 32px; 
  height: 16px; 
  animation-duration: 26s; 
  animation-delay: -20s;
  background: linear-gradient(135deg, rgba(26, 188, 156, 0.8), rgba(54, 207, 175, 0.9));
}

.fish:nth-child(8)::before { 
  border-left-color: rgba(26, 188, 156, 0.8); 
}

@keyframes swim {
  0% {
    left: -100px;
    transform: translateY(0) scaleX(1);
  }
  25% {
    transform: translateY(-20px) scaleX(1);
  }
  50% {
    transform: translateY(0) scaleX(1);
  }
  75% {
    transform: translateY(20px) scaleX(1);
  }
  100% {
    left: calc(100% + 100px);
    transform: translateY(0) scaleX(1);
  }
}

.container {
  position: relative;
  z-index: 1;
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px 32px;
}

.hero-section {
  text-align: center;
  padding: 80px 0 100px;
  animation: fadeInUp 0.8s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 10px 20px;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 50px;
  color: var(--white);
  font-size: 14px;
  font-weight: 600;
  margin-bottom: 32px;
  animation: fadeInUp 0.8s ease-out 0.2s backwards;
}

.badge-icon {
  font-size: 20px;
  animation: wave-emoji 2s ease-in-out infinite;
}

@keyframes wave-emoji {
  0%, 100% { transform: rotate(0deg); }
  25% { transform: rotate(-15deg); }
  75% { transform: rotate(15deg); }
}

.hero-title {
  font-family: 'Outfit', sans-serif;
  font-size: 72px;
  font-weight: 900;
  line-height: 1.1;
  color: var(--white);
  margin: 0 0 24px;
  letter-spacing: -2px;
  animation: fadeInUp 0.8s ease-out 0.3s backwards;
}

.highlight {
  background: linear-gradient(135deg, var(--coral), var(--coral-light));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-subtitle {
  font-size: 20px;
  color: rgba(255, 255, 255, 0.9);
  max-width: 700px;
  margin: 0 auto 60px;
  line-height: 1.6;
  font-weight: 500;
  animation: fadeInUp 0.8s ease-out 0.4s backwards;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 16px 32px;
  font-family: 'Manrope', sans-serif;
  font-size: 16px;
  font-weight: 700;
  border: none;
  border-radius: 12px;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  text-decoration: none;
}

.btn-primary {
  background: linear-gradient(135deg, var(--coral), var(--coral-light));
  color: var(--white);
  box-shadow: 0 8px 24px rgba(255, 107, 107, 0.4);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 32px rgba(255, 107, 107, 0.5);
}

.btn-primary:active {
  transform: translateY(0);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  color: var(--white);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.25);
  border-color: rgba(255, 255, 255, 0.3);
  transform: translateY(-2px);
}

.btn-large {
  padding: 20px 40px;
  font-size: 18px;
}

.btn-outline {
  background: transparent;
  border: 2px solid var(--ocean-bright);
  color: var(--ocean-bright);
}

.btn-outline:hover {
  background: rgba(46, 185, 209, 0.1);
  border-color: var(--ocean-foam);
  color: var(--ocean-foam);
}

.stats-row {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 48px;
  flex-wrap: wrap;
  padding: 40px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(30px);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 24px;
  animation: fadeInUp 0.8s ease-out 0.6s backwards;
}

.stat-item {
  text-align: center;
}

.stat-number {
  font-family: 'Outfit', sans-serif;
  font-size: 36px;
  font-weight: 800;
  color: var(--white);
  margin-bottom: 8px;
}

.stat-label {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.8);
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.stat-divider {
  width: 1px;
  height: 60px;
  background: linear-gradient(
    to bottom,
    transparent,
    rgba(255, 255, 255, 0.3),
    transparent
  );
}

.cta-section {
  margin: 100px 0 80px;
  padding: 80px 60px;
  background: linear-gradient(135deg, rgba(255, 107, 107, 0.15), rgba(255, 135, 135, 0.1));
  backdrop-filter: blur(30px);
  border: 1px solid rgba(255, 107, 107, 0.2);
  border-radius: 32px;
  text-align: center;
  animation: fadeInUp 0.8s ease-out;
}

.cta-content h2 {
  font-family: 'Outfit', sans-serif;
  font-size: 48px;
  font-weight: 800;
  color: var(--white);
  margin: 0 0 20px;
  letter-spacing: -1px;
}

.cta-content p {
  font-size: 20px;
  color: rgba(255, 255, 255, 0.9);
  margin: 0 0 40px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.cta-buttons {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

.site-footer {
  text-align: center;
  padding: 60px 20px 40px;
  color: rgba(255, 255, 255, 0.8);
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.site-footer p {
  margin: 0 0 12px;
  font-size: 18px;
  font-weight: 600;
}

.footer-credit {
  font-size: 14px;
  color: rgba(255, 255, 255, 0.6);
  font-weight: 400;
}

@media (max-width: 768px) {
  .container {
    padding: 40px 20px;
  }

  .hero-section {
    padding: 60px 0 80px;
  }

  .hero-title {
    font-size: 48px;
  }

  .hero-subtitle {
    font-size: 18px;
  }

  .stats-row {
    gap: 24px;
    padding: 32px 20px;
  }

  .stat-divider {
    display: none;
  }

  .stat-number {
    font-size: 28px;
  }

  .cta-section {
    padding: 60px 32px;
  }

  .cta-content h2 {
    font-size: 36px;
  }

  .cta-content p {
    font-size: 18px;
  }
}
</style>