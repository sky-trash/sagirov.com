<script>
export default {
  name: 'QuestionsSection',
  data() {
    return {
      questions: [
        {
          title: "Код поставки",
          description: "Обеспечение безопасной доставки и развертывания кода в production-среде"
        },
        {
          title: "Код поставки", 
          description: "Автоматизированные пайплайны для надежной доставки программного обеспечения"
        },
        {
          title: "Код поставки",
          description: "Контроль версий и управление релизами с максимальной безопасностью"
        },
        {
          title: "Код поставки",
          description: "Интеграция с системами мониторинга и оповещения о нарушениях"
        }
      ]
    }
  }
}
</script>

<template>
  <section class="questions">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Высокий, которые получают чаще всего</h2>
        <p class="section-subtitle">Самые популярные вопросы о защите кода</p>
      </div>

      <div class="questions-grid">
        <div class="question-card main-question">
          <div class="question-number">01</div>
          <h3 class="question-title">Защита крепкого кода</h3>
          <p class="question-description">Комплексные решения для обеспечения максимальной безопасности вашего исходного кода</p>
          <ul class="question-features">
            <li>Шифрование AES-256</li>
            <li>Многофакторная аутентификация</li>
            <li>Мониторинг в реальном времени</li>
          </ul>
        </div>

        <div class="questions-list">
          <div class="question-item" v-for="(question, index) in questions" :key="index">
            <div class="item-header">
              <span class="item-number">{{ index + 1 }}.</span>
              <h4 class="item-title">Код поставки</h4>
            </div>
            <p class="item-description">Обеспечение безопасной доставки и развертывания кода в production-среде</p>
            <div class="item-features">
              <span class="feature-tag">CI/CD</span>
              <span class="feature-tag">Docker</span>
              <span class="feature-tag">Kubernetes</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.questions {
  padding: 80px 0;
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .section-header {
    text-align: center;
    margin-bottom: 4rem;
    color: white;

    .section-title {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 1rem;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    }

    .section-subtitle {
      font-size: 1.2rem;
      opacity: 0.9;
    }
  }

  .questions-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  .question-card {
    background: rgba(255, 255, 255, 0.95);
    padding: 2.5rem;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    position: relative;
    overflow: hidden;

    &.main-question {
      background: linear-gradient(135deg, #00ff88, #00ccff);
      color: white;

      .question-number {
        color: rgba(255, 255, 255, 0.2);
      }
    }

    .question-number {
      position: absolute;
      top: 1rem;
      right: 1rem;
      font-size: 4rem;
      font-weight: 900;
      color: rgba(0, 0, 0, 0.1);
      line-height: 1;
    }

    .question-title {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }

    .question-description {
      font-size: 1.1rem;
      margin-bottom: 1.5rem;
      opacity: 0.9;
    }

    .question-features {
      list-style: none;

      li {
        padding: 0.5rem 0;
        position: relative;
        padding-left: 1.5rem;

        &::before {
          content: '✓';
          position: absolute;
          left: 0;
          color: #00ff88;
          font-weight: bold;
        }
      }
    }
  }

  .questions-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .question-item {
    background: rgba(255, 255, 255, 0.95);
    padding: 1.5rem;
    border-radius: 15px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;

    &:hover {
      transform: translateY(-5px);
    }

    .item-header {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      margin-bottom: 0.5rem;
    }

    .item-number {
      font-size: 1.2rem;
      font-weight: 700;
      color: #00ff88;
    }

    .item-title {
      font-size: 1.2rem;
      font-weight: 600;
      color: #333;
    }

    .item-description {
      color: #666;
      margin-bottom: 1rem;
      line-height: 1.5;
    }

    .item-features {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
    }

    .feature-tag {
      background: linear-gradient(45deg, #00ff88, #00ccff);
      color: white;
      padding: 0.3rem 0.8rem;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 600;
    }
  }

  @media (max-width: 968px) {
    .questions-grid {
      grid-template-columns: 1fr;
    }

    .section-title {
      font-size: 2rem !important;
    }

    .question-card {
      padding: 2rem;
    }
  }

  @media (max-width: 480px) {
    .container {
      padding: 0 1rem;
    }

    .section-title {
      font-size: 1.8rem !important;
    }

    .question-card {
      padding: 1.5rem;
    }

    .question-title {
      font-size: 1.5rem !important;
    }
  }
}
</style>