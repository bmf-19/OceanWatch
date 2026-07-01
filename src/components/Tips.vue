<template>
  <section class="content-card tips-card">
    <div class="card-icon-wrapper">
      <div class="icon-circle action">
        <span class="card-icon">💡</span>
      </div>
    </div>
    <div class="card-content">
      <h2>Environmental Tips</h2>
      <p class="intro-text">
        Small changes in our daily habits can create a massive impact. Here are practical steps you can take today to reduce microplastic pollution.
      </p>
      
      <div class="action-list">
        <div class="action-item">
          <div class="action-number">1</div>
          <div class="action-content">
            <h3>Choose reusable alternatives</h3>
            <p>Bring your own bags, bottles, and containers to reduce single-use plastic consumption.</p>
          </div>
        </div>

        <div class="action-item">
          <div class="action-number">2</div>
          <div class="action-content">
            <h3>Avoid single-use plastics</h3>
            <p>Skip straws, cutlery, and disposable packaging whenever possible.</p>
          </div>
        </div>

        <div class="action-item">
          <div class="action-number">3</div>
          <div class="action-content">
            <h3>Wash clothes wisely</h3>
            <p>Use a laundry bag for synthetic fabrics and wash less frequently to reduce microfiber release.</p>
          </div>
        </div>

        <div class="action-item">
          <div class="action-number">4</div>
          <div class="action-content">
            <h3>Support better products</h3>
            <p>Look for brands that use recycled materials and minimal packaging.</p>
          </div>
        </div>

        <div class="action-item">
          <div class="action-number">5</div>
          <div class="action-content">
            <h3>Spread awareness</h3>
            <p>Talk to others and share information on social media to amplify the impact.</p>
          </div>
        </div>
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
  animation: slideInUp 0.8s ease-out 0.4s backwards;
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

.tips-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 6px;
  background: linear-gradient(90deg, #4a9d5f, #66d9a8, #7ee5b8);
  border-radius: 28px 28px 0 0;
}

.card-icon-wrapper {
  margin-bottom: 32px;
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

.icon-circle.action {
  background: linear-gradient(135deg, #4a9d5f, #66d9a8);
  box-shadow: 0 8px 24px rgba(74, 157, 95, 0.3);
  animation: glow 3s ease-in-out infinite;
}

@keyframes glow {
  0%, 100% {
    transform: scale(1);
    box-shadow: 0 8px 24px rgba(74, 157, 95, 0.3);
  }
  50% {
    transform: scale(1.05);
    box-shadow: 0 12px 32px rgba(74, 157, 95, 0.4);
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

.action-list {
  display: grid;
  gap: 20px;
}

.action-item {
  display: flex;
  gap: 24px;
  padding: 28px 32px;
  background: linear-gradient(135deg, rgba(74, 157, 95, 0.06), rgba(102, 217, 168, 0.04));
  border: 1px solid rgba(74, 157, 95, 0.2);
  border-radius: 20px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  animation: slideInLeft 0.6s ease-out backwards;
  position: relative;
  overflow: hidden;
}

.action-item:nth-child(1) { animation-delay: 0.5s; }
.action-item:nth-child(2) { animation-delay: 0.6s; }
.action-item:nth-child(3) { animation-delay: 0.7s; }
.action-item:nth-child(4) { animation-delay: 0.8s; }
.action-item:nth-child(5) { animation-delay: 0.9s; }

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(40px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.action-item::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 4px;
  background: linear-gradient(180deg, #4a9d5f, #66d9a8);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.action-item:hover {
  background: linear-gradient(135deg, rgba(74, 157, 95, 0.12), rgba(102, 217, 168, 0.08));
  border-color: rgba(74, 157, 95, 0.4);
  transform: translateX(-8px);
  box-shadow: 0 8px 24px rgba(10, 36, 66, 0.1);
}

.action-item:hover::before {
  opacity: 1;
}

.action-number {
  flex-shrink: 0;
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, var(--ocean-mid), var(--ocean-bright));
  color: var(--white);
  font-family: 'Outfit', sans-serif;
  font-size: 22px;
  font-weight: 800;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  box-shadow: 0 4px 16px rgba(24, 145, 172, 0.3);
}

.action-content {
  flex: 1;
}

.action-content h3 {
  font-family: 'Outfit', sans-serif;
  font-size: 20px;
  font-weight: 700;
  color: var(--ocean-deep);
  margin: 0 0 8px;
}

.action-content p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-secondary);
  margin: 0;
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

  .action-item {
    flex-direction: column;
    padding: 24px;
    gap: 16px;
  }

  .action-number {
    width: 40px;
    height: 40px;
    font-size: 18px;
  }

  .action-content h3 {
    font-size: 18px;
  }
}
</style>