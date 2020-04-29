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
      <div class="container combos-content position-relative">
        <!-- combos -->
        <div class="row align-content-center">
          <div class="col-12">
            <h2 class="combos-content__title pb-5 text-right">Combos y Especiales</h2>
          </div>
          <div class="col-3 custom-card" @mouseenter="showCombo">
            <div class="custom-card__wrapper">
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">
                  <h3>Combo 1</h3>
                </div>
                <div class="custom-card__price">
                  <h3 class="price">
                    <span class="price__currency">$</span>
                    <span class="price__unidad">49.</span>
                    <span class="price__centena">90</span>
                  </h3>
                </div>
                <ul class="custom-card__items list-unstyled">
                  <li class="custom-card__item">Pizza Chica</li>
                  <li class="custom-card__item">Refresco 355ml</li>
                </ul>
              </div>
              <div
                class="custom-card__card-overlay position-absolute h-100 w-100 d-flex flex-column justify-content-center align-items-center"
              >
                <img src="@/static/img/pizza.png" class="img-fluid" alt>
                <h2 class="pt-2">Combo 1</h2>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card" @mouseenter="showCombo">
            <div class="custom-card__wrapper">
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">
                  <h3>Combo 2</h3>
                </div>
                <div class="custom-card__price">
                  <h3 class="price">
                    <span class="price__currency">$</span>
                    <span class="price__unidad">99.</span>
                    <span class="price__centena">90</span>
                  </h3>
                </div>
                <ul class="custom-card__items list-unstyled">
                  <li class="custom-card__item">Pizza Grande</li>
                  <li class="custom-card__item">2 Refrescos 355ml</li>
                </ul>
              </div>
              <div
                class="custom-card__card-overlay position-absolute h-100 w-100 d-flex flex-column justify-content-center align-items-center"
              >
                <img src="@/static/img/pizza.png" class="img-fluid" alt>
                <h2 class="pt-2">Combo 2</h2>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card" @mouseenter="showCombo">
            <div class="custom-card__wrapper">
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">
                  <h3>Combo 3</h3>
                </div>
                <div class="custom-card__price">
                  <h3 class="price">
                    <span class="price__currency">$</span>
                    <span class="price__unidad">269.</span>
                    <span class="price__centena">90</span>
                  </h3>
                </div>
                <ul class="custom-card__items list-unstyled">
                  <li class="custom-card__item">3 Pizzas Grandes</li>
                  <li class="custom-card__item">2 Refrescos 1.5l</li>
                </ul>
              </div>
              <div
                class="custom-card__card-overlay position-absolute h-100 w-100 d-flex flex-column justify-content-center align-items-center"
              >
                <img src="@/static/img/pizza.png" class="img-fluid" alt>
                <h2 class="pt-2">Combo 3</h2>
              </div>
            </div>
          </div>
          <div class="col-3 custom-card" @mouseenter="showCombo">
            <div class="custom-card__wrapper">
              <!-- body -->
              <div class="custom-card__body position-relative">
                <div class="custom-card__name">
                  <h3>Combo 4</h3>
                </div>
                <div class="custom-card__price">
                  <h3 class="price">
                    <span class="price__currency">$</span>
                    <span class="price__unidad">349.</span>
                    <span class="price__centena">90</span>
                  </h3>
                </div>
                <ul class="custom-card__items list-unstyled">
                  <li class="custom-card__item">4 Pizzas Grandes</li>
                  <li class="custom-card__item">3 Refrescos 1.5l</li>
                </ul>
              </div>
              <div
                class="custom-card__card-overlay position-absolute h-100 w-100 d-flex flex-column justify-content-center align-items-center"
              >
                <img src="@/static/img/pizza.png" class="img-fluid" alt>
                <h2 class="pt-2">Combo 4</h2>
              </div>
            </div>
          </div>
        </div>
        <!-- specials -->
        <div class="specials">
          <div class="special-box">
            <h3 class="special-box__title">
              <span class="accent">Miercoles</span>
              Hawaiiana
            </h3>
            <p class="special-box__price">
              <span class="accent">$</span>159.
              <span class="cents">90</span>
            </p>
            <ul class="special-box__pieces">
              <li class="special-box__piece">
                2 Pizza
                <span class="accent">GRANDES</span>
              </li>
              <li class="special-box__piece">Refresco de 1.5l</li>
            </ul>
          </div>
          <div class="special-box">
            <h3 class="special-box__title">
              <span class="accent">Jueves</span>
              Pepperoni
            </h3>
            <p class="special-box__price">
              <span class="accent">$</span>159.
              <span class="cents">90</span>
            </p>
            <ul class="special-box__pieces">
              <li class="special-box__piece">
                2 Pizza
                <span class="accent">GRANDES</span>
              </li>
              <li class="special-box__piece">Refresco de 1.5l</li>
            </ul>
          </div>
          <div class="special-box special-box--without-title">
            <p class="special-box__price">
              <span class="accent">$</span>15.
              <span class="cents">00</span>
            </p>
            <p class="special-box__description">
              Con la compra de cualquier pizza
              <span class="accent">más</span> 15 pesos te llevas
              <span class="accent">un Refresco de 1.5l</span>
            </p>
            <p></p>
          </div>
        </div>
      </div>
    </section>

    <!-- promotions -->
    <section id="promotions" class="section-block section-block__promotions row position-relative">
      <div class="container">
        <div class="row h-100 align-items-center">
          <div class="col h-100 d-flex justify-content-center align-items-center position-relative">
            <div class="wrapper-promo">
              <h2>¡Promociones!</h2>
            </div>
            <div class="position-absolute box-promotions">
              <img src="@/static/img/extra-grande.png" class="img-fluid" alt>
              <img src="@/static/img/grande.png" class="img-fluid" alt>
              <img src="@/static/img/mediana.png" class="img-fluid" alt>
              <img src="@/static/img/pequeña.png" class="img-fluid" alt>
            </div>
          </div>
          <div class="col promotions-block position-relative">
            <div class="layout-elements position-absolute overflow-hidden">
              <div class="pizzas position-absolute">
                <div class="pizzas__img">
                  <img src="@/static/img/pizza.png" class="img-fluid" alt>
                </div>
                <div class="pizzas__img">
                  <img src="@/static/img/pizza.png" class="img-fluid" alt>
                </div>
              </div>
            </div>
            <div class="wrapper-promotion d-flex justify-content-center position-relative">
              <h2 class="promotion-message text-right">
                <span class="promotion-message__quantity">2</span> pizzas grandes por
                <span class="promotion-message__price">
                  <span class="promotion-message__currency">$</span>160
                </span>
              </h2>
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
      combos: [
        {
          id: 1,
          name: "Combo 1",
          price: "$49.90",
          pieces: [{ name: "Pizza chica" }, { name: "Refresco 355ml" }],
          img: require("@/static/img/pizza.png")
        },
        {
          id: 2,
          name: "Combo 2",
          price: "$99.90",
          pieces: [{ name: "Pizza Grande" }, { name: "2 Refrescos 355ml" }],
          img: require("@/static/img/pizza.png")
        },
        {
          id: 3,
          name: "Combo 3",
          price: "$269.90",
          pieces: [{ name: "3 Pizzas Grandes" }, { name: "2 Refrescos 1.5l" }],
          img: require("@/static/img/pizza.png")
        },
        {
          id: 4,
          name: "Combo 4",
          price: "$349.90",
          pieces: [{ name: "4 Pizzas Grandes" }, { name: "3  Refrescos 1.5l" }],
          img: require("@/static/img/pizza.png")
        }
      ],
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
      patternSelect: "pattern3"
    };
  },
  methods: {
    showCombo(event) {
      const element = event.target.closest(".custom-card");
      const elements = document.querySelectorAll(".custom-card");
      elements.forEach(el => {
        el.classList.remove("open");
      });
      element.classList.toggle("open");
    }
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
        background: url("~@/static/img/pizza_pattern2.png");
        background-size: 250px;
      }
    }
    &.pattern3 {
      &::after {
        background: linear-gradient(
            180deg,
            $primary,
            transparent,
            transparent,
            transparent,
            transparent,
            transparent,
            transparent,
            white
          ),
          url("~@/static/img/pizza_pattern4.png");
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
// theme start
.combos-content {
  display: grid;
  grid-template-rows: 65% 1fr;
  z-index: 200;
  &__title {
    color: $primary;
  }
  .custom-card {
    height: 275px;
    &__wrapper {
      background-color: $secondary;
      display: grid;
      height: 100%;
      width: 250px;
      margin: 0 auto;
      box-shadow: 1px 1px 4px rgba(black, 0.25);
      border-radius: 10px;
      overflow: hidden;
      position: relative;
    }
    h3,
    li,
    span {
      color: $accent-3;
    }
    &__body {
      padding: 3rem 1rem;
      display: grid;
      grid-template-rows: repeat(5, 1fr);
      grid-template-columns: repeat(3, 1fr);
      overflow: hidden;
      position: relative;
      &::after {
        content: "";
        position: absolute;
        width: 100%;
        height: 10px;
        background-color: $primary;
        bottom: 0;
        left: 0;
      }
    }
    &__name {
      grid-column: 1 / -1;
      justify-self: center;
      align-self: center;
      font-weight: bold;
      color: $accent-3;
      font-size: 18pt;
      text-transform: uppercase;
      h3 {
        color: currentColor;
      }
    }
    &__price {
      grid-column: 1 / 4;
      grid-row: 3 / 4;
      align-self: center;
      justify-self: center;
      z-index: 100;
      position: relative;
      font-weight: bold;
      font-size: 25pt;
      color: $primary;
      h3,
      span {
        color: currentColor;
      }
      .price {
        display: flex;
        text-shadow: 0px 2px 0px white;
        &__currency {
          color: $accent-3;
          margin-right: 0.5rem;
          font-size: 20pt;
        }
        &__centena {
          font-size: 10pt;
        }
      }
    }
    &__card-overlay {
      background-color: $primary;
      z-index: 150;
      transform: translateY(0);
      transition: transform 0.5s ease, background-color, 0.5s ease;
      img {
        width: 50%;
      }
    }
    &__items {
      grid-row: 5 / 6;
      grid-column: 1 / 4;
      align-self: center;
      text-align: center;
    }
    &__item {
      font-weight: bold;
      z-index: 100;
      position: relative;
      font-size: 11pt;
      text-shadow: 0px 1px 0px white;
    }
    &.open {
      .custom-card {
        &__card-overlay {
          transform: translateY(-100%);
        }
      }
    }
    &:not(.open) {
      .custom-card {
        &__card-overlay {
          background-color: darken($primary, 5);
        }
      }
    }
  }
  .specials {
    width: 75%;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 2rem;
    margin: 1rem auto 0.5rem;
    .special-box {
      background-color: $secondary;
      color: $accent-3;
      border: 3px solid #dceee5;
      box-shadow: 0px 5px 5px #dceee5;
      border-radius: 20px;
      padding: 1.5rem;
      display: grid;
      &__piece,
      &__pieces,
      &__price,
      &__title,
      &__description {
        color: currentColor;
        font-weight: bold;
      }
      &__piece,
      &__description {
        font-size: 11pt;
        text-align: right;
        align-self: end;
      }
      &__price {
        font-weight: bold;
        font-size: 22pt;
        letter-spacing: -1px;
        display: flex;
        .cents {
          font-size: 14pt;
          color: $primary;
        }
      }
      &__title {
        text-transform: uppercase;
        width: min-content;
      }
      &--without-title {
      }
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

// ref
.promotions-block {
  .layout-elements {
    width: 100%;
    height: 350px;
    background: radial-gradient(
      circle at bottom right,
      darken($primary, 10),
      darken($primary, 2),
      $primary
    );
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-top-left-radius: 50px;
    border-bottom-right-radius: 50px;
    border-bottom-left-radius: 150px;
    border-top-right-radius: 150px;
    .pizzas {
      width: 300px;
      height: 200px;
      bottom: 0;
      right: 0;
      transform: translate(15%, 35%);
      &__img {
        width: 200px;
        position: absolute;
      }
      &__img:nth-child(1) {
        z-index: 100;
        img {
          filter: drop-shadow(18px 15px 3px rgba(8, 30, 2, 0.2));
        }
      }
      &__img:nth-child(2) {
        transform: translateX(50%);
        filter: blur(1px);
        opacity: 0.9;
      }
    }
  }
}
.section-block__promotions {
  .box-promotions {
    bottom: 0;
    width: 100%;
    height: 150px;
    display: flex;
    img {
      width: auto;
    }
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
