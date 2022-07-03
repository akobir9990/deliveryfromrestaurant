<template>
  <div class="footerVue">
    <div class="container">
      <div class="footerBox">
        <div class="box left">
          <div class="boxSection" v-for="left in lefts" :key="left.id">
            <img :src="getImageUrl(left.icon)" alt="" class="boxImg" />
            <p class="boxtext">{{ left.title }}</p>
          </div>
        </div>
        <div class="box center">
          <div class="boxSection" v-for="center in centers" :key="center.id">
            <img :src="getImageUrl(center.icon)" alt="" class="boxImg" />
            <p class="boxtext">{{ center.title }}</p>
          </div>
        </div>
        <div class="box right">
          <div class="boxSection" v-for="right in rights" :key="right.id">
            <img :src="getImageUrl(right.icon)" alt="" class="boxImg" />
            <p class="boxtext">{{ right.title }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lefts: [
        { id: 1, title: "WhatsApp", icon: "whatsApp.png" },
        { id: 2, title: "+7 (945) 450-46-60", icon: "phoneIcon.svg" },
        { id: 3, title: "Написать на E-mail", icon: "mailIcon.svg" },
      ],

      centers: [
        {
          id: 1,
          title: "Меню для частных клиентов ",
          icon: "MenuForPrivateClients.svg",
        },
        {
          id: 2,
          title: "Меню для корпоративных заказов",
          icon: "MenuForCorporateOrders.svg",
        },
        { id: 3, title: "О доставке", icon: "AboutDelivery.svg" },
      ],
      rights: [
        {
          id: 1,
          title: "Политика конфиденциальности",
          icon: "politicsPolise.svg",
        },
        {
          id: 2,
          title: "Пользовательское соглашение",
          icon: "signatureIcon.svg",
        },
        { id: 3, title: "2022 COOOK service", icon: "c.png" },
      ],
    };
  },
  methods: {
    getImageUrl(pic) {
      return require("../assets/footer/" + pic);
    },
  },
};
</script>

<style scoped lang="scss">
.footerBox {
  display: flex;
  justify-content: space-between;
  margin-top: 80px;
  flex-wrap: wrap;
  margin-bottom: 50px;

  .box {
    width: 32%;
    .boxSection {
      border-top: 1px solid #16161614;
      margin-top: 15px;
      padding-top: 5px;
      display: flex;
      align-items: center;
      p {
        border-radius: nullpx;
        font-family: Gilroy;
        font-size: 18px;
        font-weight: 300;
        line-height: 20px;
        
        cursor: pointer;
        &:hover {
          color: rgb(29, 165, 29);
        }
      }
      img {
        width: 20px;
        margin: 0px 10px;
        cursor: pointer;
      }
    }
  }
}
</style>
