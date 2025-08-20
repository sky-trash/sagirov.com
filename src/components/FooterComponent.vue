<script>
export default {
  name: 'FooterComponent'
}
</script>

<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-info">
          <h3>WeaponNet</h3>
          <p>Защита вашего кода — наша главная миссия</p>
        </div>
        <div class="footer-links">
          <a href="#">Политика конфиденциальности</a>
          <a href="#">Условия использования</a>
          <a href="#">Контакты</a>
        </div>
        <div class="footer-copyright">
          <p>&copy; 2024 WeaponNet. Все права защищены.</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  background: rgba(0, 0, 0, 0.9);
  color: white;
  padding: 2rem 0;
  margin-top: auto;

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }

  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
  }

  .footer-info {
    h3 {
      color: #00ff88;
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }

    p {
      opacity: 0.8;
    }
  }

  .footer-links {
    display: flex;
    gap: 1.5rem;

    a {
      color: white;
      text-decoration: none;
      transition: color 0.3s ease;

      &:hover {
        color: #00ff88;
      }
    }
  }

  .footer-copyright {
    opacity: 0.7;
  }

  @media (max-width: 768px) {
    .footer-content {
      flex-direction: column;
      text-align: center;
    }

    .footer-links {
      flex-direction: column;
      gap: 1rem;
    }
  }
}
</style>