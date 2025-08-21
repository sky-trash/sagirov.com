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
          <router-link to="#home" class="form-nav-home">
            <h1>Главаня</h1>
          </router-link>
          <div class="form-nav-group">
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
          </div>
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

<style lang="scss" scoped>
.header {
  padding: 20px;

  &__content {
    display: flex;
    justify-content: space-between;
    align-items: center;

    &__navigations {
      border-radius: 100px;
      width: 772px;
      height: 78px;
      background: #e9edf3;

      .form-group {
        display: flex;
        padding: 16px 0 13px 17px;

        .form-nav-home {
          border-radius: 100px;
          padding: 15.5px 21.5px;
          width: 111px;
          height: 49px;
          background: #17be79;

          h1 {
            font-family: var(--font-family);
            font-weight: 400;
            font-size: 18px;
            line-height: 100%;
            color: #fff;
          }
        }

        .form-nav-group {
          display: flex;
          justify-content: space-between;
          padding: 14px 0 17px 20px;
          width: 594px;

          .form-nav {

            h1 {
              font-family: var(--font-family);
              font-weight: 400;
              font-size: 18px;
              line-height: 100%;
              color: #272b37;
            }
          }

          // router-link:hover {
          //   border-radius: 100px;
          //   width: 111px;
          //   height: 49px;
          //   background: #17be79;
          //   padding: 14px 0 17px 20px;
          //   margin: -14px 0 -17px 0px;

          //   h1 {
          //     color: #fff;
          //   }
          // }
        }
      }
    }

    &__button {
      width: 182px;
      display: flex;
      justify-content: space-between;
    }
  }
}
</style>