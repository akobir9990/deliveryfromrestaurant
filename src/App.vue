<template>
  <div class="app">
    <div class="container">
      <HeaderNavVue />
      <nav id="navigation">
        <div class="rout">
          <router-link to="/">Частным клиентам</router-link>
          <router-link to="/about">Корпоративные заказы</router-link>
        </div>
        <div class="mainBtns">
          <button
            @click="btn.clicked = !btn.clicked"
            :class="{ click: btn.clicked }"
            class="btn"
            v-for="btn in mainBtns"
            :key="btn.index"
          >
            {{ btn.name }}
          </button>
        </div>
      </nav>
      <router-view />
      <FooterVue />
    </div>
  </div>
</template>
<script>
import HeaderNavVue from "./components/HeaderNavVue.vue";
import FooterVue from "./components/FooterVue.vue";
export default {
  components: {
    HeaderNavVue,
    FooterVue,
  },
  data() {
    return {
      mainBtns: [
        { id: 1, name: "Любимое", clicked: false },
        { id: 2, name: "Закуски", clicked: false },
        { id: 3, name: "Салаты", clicked: false },
        { id: 4, name: "Горячее", clicked: false },
        { id: 5, name: "Суши и роллы", clicked: false },
        { id: 6, name: "Супы", clicked: false },
        { id: 7, name: "Детское", clicked: false },
        { id: 8, name: "Десерты", clicked: false },
        { id: 9, name: "Напитки", clicked: false },
      ],
    };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;500;600;700;800&display=swap");
* {
  padding: 0;
  box-sizing: border-box;
  margin: 0;
}
body {
  background: #e4e4e4;
}
#app {
  font-family: Open Sans;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.container {
  max-width: 1105px;
  margin: 0 auto;
}

#navigation {
  margin: 80px 0;
  // border: 1px solid red;
  .mainBtns {
    margin-top: 30px;
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  .mainBtns .btn {
    height: 38px;
    width: 105px;
    font-size: 13px;
    font-weight: 300;
    border: none;
    border-radius: 99px;
    background: #e9e9e9;
    transition: 0.2s;
    box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.08),
      -1px -1px 6px rgba(255, 255, 255, 0.5), -5px -5px 20px #ffffff,
      5px 5px 20px #d3d3d3;
    &:hover {
      transform: scale(1.05);
      cursor: pointer;
      color: #fd9002;
    }

    &.click {
      box-shadow: inset -1px -1px 3px rgba(255, 255, 255, 0.8),
        inset -6px -6px 5px rgba(255, 255, 255, 0.3),
        inset 1px 1px 3px rgba(0, 0, 0, 0.15),
        inset 6px 6px 5px rgba(0, 0, 0, 0.06);
      background: #e9e9e9;
      color: #fd9002;
      font-weight: bold;
    }
  }
  a {
    text-decoration: none;
    font-weight: bold;
    padding: 15px;

    text-align: left;
    color: #5d6164;

    &.router-link-exact-active {
      color: #fd9002;
    }
  }
}
</style>
