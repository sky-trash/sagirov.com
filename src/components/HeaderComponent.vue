<script>
export default {
  name: 'HeaderComponent'
}
</script>

<template>
  <header class="header">
    <div class="header__content">
      <div class="header__content__logo">
        <router-link to="/">
          <img src="../../public/logo.svg" alt="">
        </router-link>
      </div>
      <div class="header__content__navigations">
        <nav class="form-group">
          <router-link to="#home" class="form-nav">
            <h1>Главаня</h1>
          </router-link>
          <router-link to="#catalog" class="form-nav">
            <h1>Каталог</h1>
          </router-link>
          <router-link to="#brands" class="form-nav">
            <h1>Бренды</h1>
          </router-link>
          <router-link to="#deliveryAndPayment" class="form-nav">
            <h1>Доставка и оплата</h1>
          </router-link>
          <router-link to="#help" class="form-nav">
            <h1>Помощь</h1>
          </router-link>
          <router-link to="#company" class="form-nav">
            <h1>Компания</h1>
          </router-link>
        </nav>
      </div>
      <div class="header__content__button">
        <router-link to="#">
          <img src="../../public/search.svg" alt="">
        </router-link>
        <router-link to="#">
          <img src="../../public/like.svg" alt="">
        </router-link>
        <router-link to="#">
          <img src="../../public/basket.svg" alt="">
        </router-link>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped></style>