<template>
  <div class="position-relative">
    <div class="sky-pizza position-absolute">
      <img src="@/static/img/pizza_real.png" class="img-fluid" alt>
    </div>
    <!-- hero -->
    <section id="hero" class="wrapper__hero position-relative">
      <div class="round-overlay position-absolute">
        <div class="pizza-hero position-absolute">
          <img src="@/static/img/pizza.png" class="img-fluid" alt>
        </div>
      </div>
      <div class="container">
        <div class="row section-block align-items-center">
          <div class="col section-block__welcome">
            <!-- <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3> -->
            <h1 class="pb-4">¡Pizza del horno a tu casa!</h1>
            <a href="#our-menu" class="btn btn-primary font-weight-bold">Ver menu</a>
          </div>
          <div class="col"></div>
        </div>
      </div>
    </section>

    <!-- combos and specials -->
    <section id="combos-and-specials" class="section-block section-block__combos row">
      <div class="container combos-content">
        <div class="row h-100 align-content-center">
          <div class="col-12">
            <h2 class="combos-content__title pb-5 text-right">Combos y Especiales</h2>
          </div>
          <div class="col-3 custom-card">
            <div class="custom-card__wrapper">
              <!-- head -->
              <div class="custom-card__img">imagen</div>
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">Nombre</div>
                <ul class="custom-card__ingredients">
                  <li
                    class="custom-card__ingredient"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
                </ul>
                <div class="custom-card__price position-absolute"></div>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card">
            <div class="custom-card__wrapper">
              <!-- head -->
              <div class="custom-card__img">imagen</div>
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">Nombre</div>
                <ul class="custom-card__ingredients">
                  <li
                    class="custom-card__ingredient"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
                </ul>
                <div class="custom-card__price position-absolute"></div>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card">
            <div class="custom-card__wrapper">
              <!-- head -->
              <div class="custom-card__img">imagen</div>
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">Nombre</div>
                <ul class="custom-card__ingredients">
                  <li
                    class="custom-card__ingredient"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
                </ul>
                <div class="custom-card__price position-absolute"></div>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card">
            <div class="custom-card__wrapper">
              <!-- head -->
              <div class="custom-card__img">imagen</div>
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">Nombre</div>
                <ul class="custom-card__ingredients">
                  <li
                    class="custom-card__ingredient"
                  >Lorem ipsum dolor sit amet consectetur adipisicing elit.</li>
                </ul>
                <div class="custom-card__price position-absolute"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- promotions -->
    <section id="promotions" class="section-block section-block__promotions row position-relative">
      <div class="layout-elements position-absolute w-100 h-100">
        <div class="layout-elements__block layout-elements__block--left"></div>
        <div class="layout-elements__block layout-elements__block--right"></div>
      </div>
      <div class="container">
        <div class="row h-100 align-items-center">
          <div class="col d-flex justify-content-center">
            <div class="wrapper-promo">
              <h2>¡Promociones!</h2>
            </div>
          </div>
          <div class="col">
            <div class="wrapper-promotion d-flex justify-content-center position-relative">
              <div class="pizzas position-absolute">
                <div class="pizzas__img">
                  <img src="@/static/img/pizza.png" class="img-fluid" alt>
                </div>
                <div class="pizzas__img">
                  <img src="@/static/img/pizza.png" class="img-fluid" alt>
                </div>
              </div>
              <h2 class="promotion-message text-right">
                <span class="promotion-message__quantity">2</span> pizzas grandes por
                <span class="promotion-message__price">
                  <span class="promotion-message__currency">$</span>160
                </span>
              </h2>
              <!-- <h2 class="promo-title">
                <span class="promo-title__word promo-title__word--promo">Promo</span>
                <span class="promo-title__word promo-title__word--quantity">2</span>
                <span class="promo-title__word promo-title__word--pizza">Pizzas</span>
                <span class="promo-title__word promo-title__word--for">por</span>
                <span class="promo-title__word promo-title__word--height">grandes</span>
                <span class="promo-title__word promo-title__word--currency">$</span>
                <span class="promo-title__word promo-title__word--price">160</span>
              </h2>-->
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- our menu -->
    <section id="our-menu" class="section-block section-block__menu row">
      <div class="container">
        <div class="row">
          <div class="col">
            <h2 class="text-center py-3 pb-5">Su menú!</h2>
            <select name="background-pattern" v-model="patternSelect">
              <option value="pattern1">Fondo 1</option>
              <option value="pattern2">Fondo 2</option>
              <option value="pattern3">Fondo 3</option>
            </select>
          </div>
        </div>
        <div class="row justify-content-around my-menu" :class="patternSelect">
          <div
            class="col-12 col-md-6 col-lg-4 orders-menu d-flex justify-content-center align-items-center my-5"
            v-for="(pizza, i) in menu"
            :key="i"
          >
            <div class="deeply-switch active-all">
              <div class="deeply-switch__back">
                <div class="deeply-switch__wrapper-body">
                  <div class="deeply-switch__title text-capitalize">{{ pizza.name }}</div>
                  <div class="deeply-switch__description">{{ pizza.description }}</div>
                </div>
              </div>
              <div class="deeply-switch__front">
                <img src="@/static/img/pizza.png" class="img-fluid" alt>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  scrollToTop: true,
  layout: "pizzeria",
  data() {
    return {
      menu: [
        {
          id: "",
          name: "Hawaiiana",
          description: "Jamón, piña cereza, ex. queso"
        },
        {
          id: "",
          name: "pepperoni",
          description: "Extra pepperoni extra queso"
        },
        {
          id: "",
          name: "vegetariana",
          description: "Champiñon, piña, pimiento,cebolla"
        },
        {
          id: "",
          name: "Ranchera",
          description: "Frijol, chorizo, cebolla,jalapeño"
        },
        {
          id: "",
          name: "Carnes frias",
          description: "Jamón, salchicha, salami, pepperoni "
        },
        {
          id: "",
          name: "Burguer",
          description: "C. molida, salami, tocino, q. amarillo"
        },
        {
          id: "",
          name: "Mexicana",
          description: "Chorizo. c. molida, jalapeño, tocino"
        },
        {
          id: "",
          name: "Del mar",
          description: "Camaron, atun, pimiento, ex. queso"
        },
        {
          id: "",
          name: "Chickén",
          description: "Jamón, pollo, champion, ex. queso"
        },
        {
          id: "",
          name: "A la diabla",
          description: "C. pastor, chipotle, jalapeño, chorizo"
        },
        {
          id: "",
          name: "Cordón blue",
          description: "Pollo, jamón, tocino, q. amarillo"
        },
        {
          id: "",
          name: "Emperatriz",
          description: "Pepperoni, pimiento, c. molida, tocina"
        },
        {
          id: "",
          name: "Marina",
          description: "Atún, elote, pimiento, cebolla"
        },
        {
          id: "",
          name: "Norteña",
          description: "Chorizo, tocino, pimiento, elote"
        },
        {
          id: "",
          name: "Romana",
          description: "Champoñon, chorizo, jalapeño, tocino"
        },
        {
          id: "",
          name: "Cubana",
          description: "Jamón, tocino, chorizo, q. amarillo"
        },
        {
          id: "",
          name: "4 quesos",
          description: "Mozarella, oaxaca, americano, gouda"
        },
        {
          id: "",
          name: "Kanter",
          description: "Champiñon, tocino, salami, peperoni"
        },
        {
          id: "",
          name: "Pastor",
          description: "C. pator, piña, cebolla, tocino"
        },
        {
          id: "",
          name: "Hawaiiana VIP",
          description: "Jamón, piña, jalapeño, tocino"
        },
        {
          id: "",
          name: "Italiana",
          description: "Jamon, salchicha, salami, pimiento"
        },
        {
          id: "",
          name: "Al gusto",
          description: "4 ingredientes al gusto"
        }
      ],
      patternSelect: ""
    };
  }
};
</script>
<style lang="scss">
.round-overlay {
  width: 100vw;
  height: 100%;
  background: linear-gradient(150deg, $primary, $primary, darken($primary, 15));
  left: 50%;
  top: 0;
  transform: translateX(-50%);
  border-bottom-right-radius: 100%;
  animation: swipeBorder 3s ease 1;
  z-index: 100;
  @keyframes swipeBorder {
    0% {
      border-bottom-right-radius: 0%;
    }
    100% {
      border-bottom-right-radius: 100%;
    }
  }
}
.deeply-switch {
  $width_front: 150px;
  position: relative;
  width: $width_front;
  &__front {
    width: $width_front;
    height: 140px;
    position: relative;
    z-index: 100;
    transition: transform 0.5s ease;
  }
  &__back {
    background-color: $secondary;
    width: 0%;
    height: 100%;
    top: 2.5px;
    left: $width_front / 2;
    position: absolute;
    transition: width 0.5s ease, transform 0.5s ease;
    border-top-right-radius: 130px;
    border-bottom-right-radius: 130px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    .deeply-switch__wrapper-body {
      width: 250px;
    }
    .deeply-switch__title,
    .deeply-switch__description {
      opacity: 0;
      color: $primary;
      width: 50%;
      margin-right: 1.5rem;
      margin-left: auto;
      transition: opacity 0.5s ease;
    }
    .deeply-switch__title {
      font-weight: bold;
      padding-bottom: 0.5rem;
    }
    .deeply-switch__description {
      color: grey;
    }
  }
  &:hover,
  &.active-all {
    .deeply-switch__front {
      transform: translateX(-50%);
    }
    .deeply-switch__back {
      width: 250px;
      transform: translateX(-35%);
      box-shadow: 0px 6px 10px rgba(black, 0.25);
    }
    .deeply-switch__title,
    .deeply-switch__description {
      opacity: 1;
    }
  }
}
body {
  background: $primary;
}
* {
  color: $secondary;
  scroll-behavior: smooth;
}
.wrapper {
  &__hero {
    background-color: $secondary;
  }
}
.section-block {
  min-height: 100vh;
  &__welcome {
    position: relative;
    z-index: 100;
  }
  &__combos {
    background-color: $secondary;
  }
  &__promotions {
    background-color: $secondary;
    // background: url("~@/static/img/pizzeria_patter.png");
    // min-height: 55vh;
  }
  &__menu {
    padding: 5rem 0 0;
    position: relative;
  }
  .my-menu {
    position: relative;
    &::after {
      content: "";
      position: absolute;
      width: 100vw;
      height: 100%;
      top: 50%;
      left: 50%;
      z-index: -1;
      transform: translate(-50%, -50%);
      opacity: 0.9;
    }
    &.pattern1 {
      &::after {
        background: url("~@/static/img/pizzeria_patter.png");
      }
    }
    &.pattern2 {
      &::after {
        content: "";
        background: url("~@/static/img/pizza_pattern2.png");
        background-size: 250px;
      }
    }
    &.pattern3 {
      &::after {
        background: url("~@/static/img/pizza_pattern4.png");
        background-size: 250px;
      }
    }
  }
}
h1 {
  font-size: 42pt;
}
h2 {
  font-size: 24pt;
}
.btn.btn-primary {
  // background-color: $blanco;
}
// theme start
.combos-content {
  //   background: url("~@/static/img/pizzeria_patter.png");
  z-index: 200;
  &__title {
    color: $primary;
  }
  .custom-card {
    height: 275px;
    &__wrapper {
      background-color: $secondary;
      display: grid;
      grid-template-rows: 55% 1fr;
      height: 100%;
      width: 200px;
      margin: 0 auto;
      box-shadow: 1px 1px 4px rgba(black, 0.25);
      border-radius: 5px;
    }
    &__img {
      background-color: grey;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__body {
      padding: 1rem;
      display: grid;
      overflow: hidden;
    }
    &__name,
    &__price,
    &__ingredient {
      color: grey;
    }
    &__name {
      font-weight: bold;
      color: $primary;
    }
    &__price {
      background-color: $primary;
      width: 100px;
      height: 100px;
      right: 0;
      bottom: 0;
      transform: translate(75%, 75%);
      border-radius: 50%;
    }
  }
}
.orders-menu {
  height: 150px;
}
.wrapper-promo {
  width: 300px;
  h2 {
    color: $primary;
  }
}
// .promo-title {
//   font-size: 35pt;
//   display: grid;
//   grid-template-columns: repeat(5, 1fr);
//   grid-template-rows: repeat(4, 1fr);
//   text-transform: capitalize;
//   height: 100%;
//   &__word--promo {
//     grid-column: 1 / 4;
//     justify-self: center;
//     align-self: flex-end;
//     font-size: 40pt;
//     color: $accent-1;
//   }
//   &__word--quantity {
//     grid-row: 2 / 4;
//     grid-column: 1 / 3;
//     font-size: 150pt;
//     justify-self: center;
//     color: $secondary;
//   }
//   &__word--pizza {
//     grid-row: 2 / 4;
//     grid-template-columns: 3 / 4;
//     writing-mode: sideways-lr;
//     color: #70ba6d;
//   }
//   &__word--for {
//     grid-column: 4 / 5;
//     grid-row: 2 / 3;
//     justify-self: center;
//     align-self: center;
//     color: #b689b0;
//   }
//   &__word--height {
//     grid-row: 4 / 5;
//     grid-column: 1 / 4;
//     font-size: 45pt;
//     justify-self: center;
//     color: #39b3b8;
//   }
//   &__word--currency {
//     grid-column: 4 / 5;
//     grid-row: 1 / 2;
//     justify-self: center;
//     align-self: flex-end;
//     color: #f2c534;
//   }
//   &__word--price {
//     color: #f2c534;
//     justify-self: center;
//     align-self: flex-end;
//   }
// }
.promotion-message {
  font-size: 27pt;
  width: min-content;
  position: relative;
  z-index: 150;
  &__quantity {
    font-size: 35pt;
  }
  &__price {
    font-size: 70pt;
  }
  &__currency {
    transform: scale(0.5);
  }
}
.layout-elements {
  display: flex;
  &__block {
    flex: 1;
    height: 100%;
  }
  &__block--right {
    margin-left: auto;
    margin-top: auto;
    margin-bottom: auto;
    background-color: $primary;
    border-top-left-radius: 600px 600px;
    animation: swipeLeft 2s ease 1;
    transform: translateX(-10%);
    flex: 0 1 40%;
    height: 50%;
    border-top-left-radius: 50px;
    border-bottom-right-radius: 50px;
    border-bottom-left-radius: 150px;
    border-top-right-radius: 150px;
  }
}
.pizzas {
  display: flex;
  top: 75%;
  left: 200px;
  &__img {
    width: 200px;
  }
  &__img:nth-child(1) {
    transform: translateX(50px);
    z-index: 100;
  }
  &__img:nth-child(2) {
    transform: translateX(-50px);
    filter: blur(1.5px);
    opacity: 0.7;
  }
}
.pizza-hero {
  top: 50%;
  left: 0;
  transform: translate(-70%, -50%);
}
.sky-pizza {
  z-index: 100;
  max-height: 150vh;
  width: 50%;
  top: 70vh;
  left: 50%;
  transform: translateX(-50%);
  img {
    filter: drop-shadow(-7px 5px 5px rgba(black, 0.25));
  }
}
// animations
@keyframes swipeLeft {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0%);
  }
}
</style>
