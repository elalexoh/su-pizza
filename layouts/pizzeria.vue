<template>
  <div class="position-relative overflow-hidden">
    <!-- header -->
    <header
      class="container layout-block layout-block__header position-absolute d-flex justify-content-between align-items-center mx-auto"
    >
      <img src="@/static/img/logoSuPizza.svg" width="125" class="img-fluid" alt>

      <!-- main menu -->
      <ul class="main-menu d-flex">
        <li class="main-menu__item" v-for="(item, index) in menuSettings.sections" :key="index">
          <!-- <a href="#hero" class="text-decoration-none text-reset">Inicio</a> -->
          <nuxt-link :to="item.link" tag="a" class="text-decoration-none text-reset">{{item.name}}</nuxt-link>
        </li>
      </ul>

      <!-- Mobile menu -->
      <ul class="mobile-menu d-none">
        <li class="mobile-menu__item">
          <a href="#hero" class="text-decoration-none text-reset">Inicio</a>
        </li>
        <li class="mobile-menu__item">
          <a href="#promotions" class="text-decoration-none text-reset">Promociones</a>
        </li>
        <li class="mobile-menu__item">
          <a href="#our-menu" class="text-decoration-none text-reset">Nuestro menu</a>
        </li>
        <li class="mobile-menu__item">
          <a href="#combos-and-specials" class="text-decoration-none text-reset">Especiales</a>
        </li>
      </ul>
    </header>

    <!-- body -->
    <nuxt/>

    <!-- footer -->
    <footer class="wrapper-footer position-relative">
      <div class="layout-block layout-block__footer container">
        <!-- sections -->
        <div class="footer-block footer-block--sections">
          <h3 class="footer-block__title">Secciones</h3>
          <ul>
            <li v-for="(section, i) in menuSettings.sections" :key="i" class="pb-2">
              <a :href="section.link" class="text-decoration-none text-reset">{{ section.name }}</a>
            </li>
          </ul>
        </div>

        <!-- direction -->
        <div class="footer-block footer-block--direction text-center">
          <h3 class="footer-block__title">Dirección</h3>
          <p class="footer-block__direction">Av. Quinceo 387 Granjas del Maestro Morelia, Mich</p>
        </div>

        <!-- phone -->
        <div class="footer-block footer-block--phones text-right">
          <h3 class="footer-block__title">Contactanos</h3>
          <ul class="footer-block__phone">
            <li class="phone__item pb-2">312.80.50</li>
            <li class="phone__item pb-2">232.29.38</li>
            <li class="phone__item pb-2">4433.51.54.66</li>
          </ul>
        </div>

        <!-- shipping -->
        <!-- <ul class="footer-block footer-block--payment-methods">
        <li class="payment-methods__method">VISA</li>
        <li class="payment-methods__method">Master Car</li>
        </ul>-->

        <!-- social Media -->
        <ul class="footer-block footer-block--social-media list-unstyled">
          <li class="social-media__item">
            <a
              href="https://www.facebook.com"
              class="text-decoration-none text-reset"
              target="_blank"
            >Facebook</a>
          </li>
          <li class="social-media__item">
            <a
              href="https://www.facebook.com"
              class="text-decoration-none text-reset"
              target="_blank"
            >Twitter</a>
          </li>
        </ul>
        <!-- copyright -->
        <div class="footer-block footer-block--copyright">2020 @ su pizzeria all rights reserved.</div>
      </div>
      <div class="footer-pizza position-absolute">
        <img src="@/static/img/pizza.png" class="img-fluid" alt>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menuSettings: {
        sections: [
          { link: "#hero", name: "Inicio" },
          { link: "#combos-and-specials", name: "Especiales" },
          { link: "#promotions", name: "Promociones" },
          { link: "#our-menu", name: "Menu" }
        ]
      }
    };
  }
};
</script>
<style lang="scss">
.wrapper-footer {
  background: linear-gradient(180deg, #008f4a, #008f4a, darken(#008f4a, 5));
}
.layout-block {
  position: relative;
  z-index: 100;
  &__header {
    top: 0;
    left: 50%;
    transform: translateX(-50%);
  }
  &__footer {
    display: grid;
    grid-template-rows: repeat(3, max-content);
    grid-template-columns: repeat(3, 1fr);
    padding: 3rem 0 2rem;
    .footer-block {
      padding: 0 1rem;
      font-size: 14pt;
      &__title {
        font-size: 18pt;
        font-weight: bolder;
        padding-bottom: 0.8rem;
      }
      &--payment-methods,
      &--copyright,
      &--social-media {
        justify-self: center;
        align-self: center;
      }
      &--payment-methods,
      &--social-media {
        display: flex;
        width: 100%;
        justify-content: space-around;
      }
      &--social-media {
        grid-column: 2 / 3;
        padding: 1rem 0;
      }
      &--copyright {
        grid-row: 3 / -1;
        grid-column: 1 / -1;
        font-size: 10pt;
        font-weight: bold;
      }
    }
  }
}
.main-menu {
  &__item {
    padding: 0.9rem;
    font-weight: bold;
  }
}
.footer-pizza {
  width: 100%;
  height: 100%;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  transform: translateY(60%) rotate(0deg);
  animation: spin 5s ease infinite;
  img {
    width: 25%;
    opacity: 0.4;
  }
  @keyframes spin {
    0% {
      transform: translateY(60%) rotate(0deg);
    }
    100% {
      transform: translateY(60%) rotate(360deg);
    }
  }
}
</style>
