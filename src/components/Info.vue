<template>
  <section class="content-card info-card">
    <div class="card-icon-wrapper">
      <div class="icon-circle warning">
        <span class="card-icon">⚠️</span>
      </div>
    </div>
    <div class="card-content">
      <h2>Why it matters</h2>
      <p class="intro-text">
        The impact of microplastics extends far beyond what we can see. Here's why this issue demands our immediate attention.
      </p>
      
      <div class="impact-grid">
        <div class="impact-item">
          <div class="impact-icon">🌊</div>
          <div class="impact-content">
            <h3>Widespread Pollution</h3>
            <p>Tiny plastic particles are found in oceans, freshwater, soil, and even inside animals and people.</p>
          </div>
        </div>
        
        <div class="impact-item">
          <div class="impact-icon">🐠</div>
          <div class="impact-content">
            <h3>Wildlife Impact</h3>
            <p>Animals can mistake microplastics for food, which can harm digestion or add toxic chemicals to their bodies.</p>
          </div>
        </div>
        
        <div class="impact-item">
          <div class="impact-icon">⏳</div>
          <div class="impact-content">
            <h3>Long-Lasting</h3>
            <p>Plastics can take hundreds of years to break down, but microplastics remain and continue to circulate.</p>
          </div>
        </div>
      </div>
      
      <div class="action-paragraph">
        <p>
          The challenge of microplastic pollution may seem overwhelming, but every individual action contributes to meaningful change. By making conscious choices in our daily lives—from the products we buy to the way we dispose of waste—we can collectively reduce the flow of microplastics into our environment. Together, we have the power to protect our oceans, preserve wildlife, and ensure a healthier planet for future generations. The time to act is now.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.content-card {
  margin: 60px 0;
  padding: 48px;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(30px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 28px;
  box-shadow: 0 20px 60px rgba(10, 36, 66, 0.15);
  position: relative;
  overflow: hidden;
  animation: slideInUp 0.8s ease-out 0.2s backwards;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.content-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 32px 80px rgba(10, 36, 66, 0.2);
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(60px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.info-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 6px;
  background: linear-gradient(90deg, #ff6b6b, #ff8787, #ffa5a5);
  border-radius: 28px 28px 0 0;
}

.card-icon-wrapper {
  margin-bottom: -40px;
}

.icon-circle {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #2eb9d1, #66d9e8);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 8px 24px rgba(46, 185, 209, 0.3);
}

.icon-circle.warning {
  background: linear-gradient(135deg, #ff6b6b, #ff8787);
  box-shadow: 0 8px 24px rgba(255, 107, 107, 0.3);
  animation: pulse 3s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}

.card-icon {
  font-size: 40px;
  filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.1));
}

.card-content h2 {
  font-family: 'Outfit', sans-serif;
  font-size: 36px;
  font-weight: 800;
  color: var(--ocean-deep);
  margin: 0 0 20px;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.intro-text {
  font-size: 18px;
  line-height: 1.7;
  color: var(--text-secondary);
  margin: 0 0 40px;
}

.impact-grid {
  display: grid;
  gap: 24px;
}

.impact-item {
  display: flex;
  gap: 24px;
  padding: 32px;
  background: linear-gradient(135deg, rgba(244, 232, 216, 0.4), rgba(230, 213, 195, 0.2));
  border: 1px solid rgba(24, 145, 172, 0.15);
  border-radius: 20px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  animation: slideInRight 0.6s ease-out backwards;
}

.impact-item:nth-child(1) { animation-delay: 0.3s; }
.impact-item:nth-child(2) { animation-delay: 0.4s; }
.impact-item:nth-child(3) { animation-delay: 0.5s; }

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(-40px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.impact-item:hover {
  background: linear-gradient(135deg, rgba(244, 232, 216, 0.6), rgba(230, 213, 195, 0.4));
  border-color: rgba(24, 145, 172, 0.3);
  transform: translateX(8px);
  box-shadow: 0 8px 24px rgba(10, 36, 66, 0.1);
}

.impact-icon {
  font-size: 48px;
  flex-shrink: 0;
  width: 64px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--white);
  border-radius: 16px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.06);
}

.impact-content h3 {
  font-family: 'Outfit', sans-serif;
  font-size: 22px;
  font-weight: 700;
  color: var(--ocean-deep);
  margin: 0 0 12px;
}

.impact-content p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-secondary);
  margin: 0;
}

.action-paragraph {
  margin-top: 40px;
  padding: 32px;
  background: linear-gradient(135deg, rgba(74, 157, 95, 0.08), rgba(102, 217, 168, 0.05));
  border-left: 4px solid #4a9d5f;
  border-radius: 16px;
  animation: fadeIn 0.8s ease-out 0.6s backwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.action-paragraph p {
  font-size: 17px;
  line-height: 1.8;
  color: var(--text-secondary);
  margin: 0;
  font-weight: 500;
}

@media (max-width: 768px) {
  .content-card {
    padding: 32px 24px;
    margin: 40px 0;
  }

  .card-content h2 {
    font-size: 28px;
  }

  .icon-circle {
    width: 64px;
    height: 64px;
  }

  .card-icon {
    font-size: 32px;
  }

  .impact-item {
    flex-direction: column;
    padding: 24px;
  }

  .impact-icon {
    width: 56px;
    height: 56px;
    font-size: 40px;
  }

  .impact-content h3 {
    font-size: 20px;
  }
}
</style>