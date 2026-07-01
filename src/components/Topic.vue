<script setup>
</script>

<template>
  <section class="content-card topic-card">
    <div class="card-icon-wrapper">
      <div class="icon-circle">
        <span class="card-icon">♻️</span>
      </div>
    </div>
    <div class="card-content">
      <h2>What are microplastics?</h2>
      <p>
        Microplastics are tiny plastic pieces (less than 5mm) that come from a wide
        range of products — from cosmetics and clothing to packaging and tyres.
        Once in the environment, they are hard to remove and can travel far.
      </p>
      <p>
        They are a major pollutant in oceans, rivers, soil and even the air we breathe.
        Understanding what they are is the first step to reducing the harm they cause.
      </p>
      <div class="card-highlight">
        <strong>Key fact:</strong> Microplastics have been found in the deepest parts of the ocean and on the highest mountains.
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
  animation: slideInUp 0.8s ease-out;
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

.topic-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 6px;
  background: linear-gradient(90deg, #1891ac, #2eb9d1, #66d9e8);
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
  animation: pulse 3s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% {
    transform: scale(1);
    box-shadow: 0 8px 24px rgba(46, 185, 209, 0.3);
  }
  50% {
    transform: scale(1.05);
    box-shadow: 0 12px 32px rgba(46, 185, 209, 0.4);
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
  margin: 0 0 28px;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.card-content p {
  font-size: 18px;
  line-height: 1.8;
  color: var(--text-secondary);
  margin: 0 0 24px;
}

.card-content p:last-of-type {
  margin-bottom: 32px;
}

.card-highlight {
  padding: 24px 28px;
  background: linear-gradient(135deg, rgba(46, 185, 209, 0.08), rgba(102, 217, 232, 0.05));
  border-left: 4px solid var(--ocean-bright);
  border-radius: 12px;
  font-size: 16px;
  line-height: 1.6;
  color: var(--text-secondary);
}

.card-highlight strong {
  color: var(--ocean-deep);
  font-weight: 700;
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
}
</style>