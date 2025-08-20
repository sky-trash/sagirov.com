<script>
export default {
  name: 'HeroSection',
  data() {
    return {
      codeLines: [
        'function protectCode() {',
        '  const security = new Firewall();',
        '  security.encrypt("strong-code");',
        '  return "protected";',
        '}',
        '// WeaponNet Security System',
        'class AdvancedProtection {',
        '  constructor() {',
        '    this.shield = true;',
        '    this.encryption = "AES-256";',
        '  }',
        '}'
      ]
    }
  }
}
</script>

<template>
  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <div class="hero-text">
          <h2 class="hero-title">
            Вопросы: негодная оборудование<br>
            для защиты крепкого кода
          </h2>
          <p class="hero-subtitle">www.weaponnet.com</p>
          <div class="hero-actions">
            <button class="btn btn-primary">Начать защиту</button>
            <button class="btn btn-secondary">Узнать больше</button>
          </div>
        </div>
        <div class="hero-visual">
          <div class="code-animation">
            <div class="code-line" v-for="(line, index) in codeLines" :key="index"
              :style="{ animationDelay: `${index * 0.2}s` }">
              {{ line }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero {
  padding: 120px 0 80px;
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .hero-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }

  .hero-text {
    color: white;

    .hero-title {
      font-size: 3rem;
      font-weight: 700;
      line-height: 1.2;
      margin-bottom: 1.5rem;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }

    .hero-subtitle {
      font-size: 1.5rem;
      color: #00ff88;
      margin-bottom: 2rem;
      font-weight: 600;
    }
  }

  .hero-actions {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }

  .btn {
    padding: 1rem 2rem;
    border: none;
    border-radius: 8px;
    font-size: 1.1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    text-transform: uppercase;
    letter-spacing: 1px;

    &-primary {
      background: linear-gradient(45deg, #00ff88, #00ccff);
      color: white;

      &:hover {
        transform: translateY(-2px);
        box-shadow: 0 10px 20px rgba(0, 255, 136, 0.3);
      }
    }

    &-secondary {
      background: transparent;
      color: white;
      border: 2px solid #00ff88;

      &:hover {
        background: #00ff88;
        color: #333;
      }
    }
  }

  .hero-visual {
    position: relative;
  }

  .code-animation {
    background: rgba(0, 0, 0, 0.8);
    padding: 2rem;
    border-radius: 12px;
    border: 1px solid #00ff88;
    box-shadow: 0 0 30px rgba(0, 255, 136, 0.2);
    font-family: 'Fira Code', 'Monaco', monospace;
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .code-line {
    color: #00ff88;
    opacity: 0;
    animation: fadeIn 0.5s ease forwards;

    &:nth-child(2n) {
      color: #00ccff;
    }

    &:nth-child(3n) {
      color: #ff6b6b;
    }
  }

  @keyframes fadeIn {
    to {
      opacity: 1;
    }
  }

  @media (max-width: 968px) {
    .hero-content {
      grid-template-columns: 1fr;
      gap: 2rem;
      text-align: center;
    }

    .hero-title {
      font-size: 2.5rem !important;
    }

    .hero-actions {
      justify-content: center;
    }

    .code-animation {
      font-size: 0.8rem;
    }
  }

  @media (max-width: 480px) {
    .hero-title {
      font-size: 2rem !important;
    }

    .hero-subtitle {
      font-size: 1.2rem !important;
    }

    .btn {
      padding: 0.8rem 1.5rem;
      font-size: 1rem;
    }
  }
}
</style>