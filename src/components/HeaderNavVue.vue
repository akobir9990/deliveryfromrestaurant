<template>
  <header class="headerVue">
    <div class="container">
      <nav class="nav">
        <div class="logo">
          <img src="../assets/header/img/logo.svg" alt="" />
        </div>
        <div class="btns">
          <button class="whatsapp">
            <img src="../assets/header/img/WhatsApp.svg" alt="" />
            WhatsApp
          </button>
          <button class="order">Заказать 1 блюдо за 430₽</button>
          <button class="profile">
            <img src="../assets/header/img/profile.svg" alt="" />
          </button>
        </div>
      </nav>
      <div class="headerContent">
        <img src="../assets/header/img/Food.png" alt="" class="food" />
        <div class="cart">
          <h1 class="cartTitle">Доставка из ресторана в керамической посуде</h1>
          <button class="playStory">
            Сториз о сервисе <img src="../assets/header/img/play.svg" alt="" />
          </button>
        </div>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  setup() {},
};
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 20px 10px;
  .btns {
    display: flex;
    .whatsapp {
      height: 40px;
      width: 179px;
      padding: 0 15px;
      display: flex;
      justify-content: space-around;
      align-items: center;
      border-radius: 30px;
      background: #25d366;
      border: none;
      color: #fff;
      //styleName: Button;
      font-family: Gilroy;
      font-size: 18px;
      font-weight: 700;
      line-height: 20px;
      letter-spacing: 0em;
      text-align: left;
    }
    .order {
      height: 40px;
      width: 280px;
      margin: 0 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 30px;
      background: #e9e9e9;
      border: none;
      box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.08),
        -1px -1px 6px rgba(255, 255, 255, 0.5), -5px -5px 20px #ffffff,
        5px 5px 20px #d3d3d3;
      border-radius: 30px;

      //styleName: 1;
      font-family: Gilroy;
      font-size: 18px;
      font-weight: 700;
      line-height: 20px;
      letter-spacing: 0em;
      text-align: left;
    }
    .profile {
      height: 40px;
      width: 40px;
      left: 1505px;
      top: 40px;
      border-radius: 0px;
      border: none;
      border-radius: 50%;
      background: #e9e9e9;
      box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.08),
        -1px -1px 6px rgba(255, 255, 255, 0.5), -5px -5px 20px #ffffff,
        5px 5px 20px #d3d3d3;
    }
  }
}
.headerContent {
  position: relative;
  margin: 20px 0;
  width: 100%;
  .food {
    position: absolute;
    top: 30px;
    right: 0;
  }
  .cart {
    height: 500px;
    width: 1105px;
    background: #212629;
    box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.05),
      40px 40px 50px rgba(0, 0, 0, 0.5);
    border-radius: 80px 80px 80px 5px;
    .cartTitle {
      height: 238px;
      width: 565.25px;
      left: 425px;
      top: 200px;
      padding: 50px 0 0 50px;

      font-family: Gilroy;
      font-size: 50px;
      font-weight: 700;
      line-height: 62px;
      letter-spacing: 0em;
      text-align: left;

      color: #ffffff;
    }
    .playStory {
      height: 40px;
      width: 230px;
      display: flex;
      margin: 50px 0 0 50px;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px 0 30px;
      flex-direction: row;
      border-radius: 99px;

      background: #212629;
      border: none;
      box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5),
        -1px -1px 6px rgba(255, 255, 255, 0.05),
        -5px -5px 20px rgba(255, 255, 255, 0.1), 5px 5px 20px rgba(0, 0, 0, 0.8);
      border-radius: 99px;

      border-radius: nullpx;
      //styleName: Button;
      font-family: Gilroy;
      font-size: 18px;
      font-weight: 700;
      line-height: 20px;
      letter-spacing: 0em;
      text-align: left;
      color: #fe9102;
    }
  }
}
</style>
