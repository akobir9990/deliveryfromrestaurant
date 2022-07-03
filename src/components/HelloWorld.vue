<template>
  <div class="content">
    <div class="container">
      <div class="snaks">
        <h1 class="title">Закуски</h1>
        <div class="cart" v-for="cart in carts" :key="cart.id">
          <div class="cartTop" :style="{ 'background-color': cart.bgColor }">
            <img :src="getImage(cart.imgUrl)" alt="" />
            <label for="heart" class="heart">
              <input type="checkbox" name="" id="heart" />
              <div class="path" @click="cart.liked = !cart.liked">
                <svg>
                  <path :d="cart.heart" :class="{ like: cart.liked }"></path>
                </svg>
              </div>
            </label>
          </div>
          <div class="Info">
            <h1 class="cartTitle">{{ cart.title }}</h1>
            <div class="cartInfo">
              <ul class="infoList">
                <li class="listItem">{{ cart.gramm }}</li>
                <li class="listItem">{{ cart.kkal }}</li>
                <li class="listItem price">{{ cart.price }}</li>
              </ul>
              <p class="cartText">
                Это вкусное и сытное блюдо является любимым блюдом во многих
                семьях, полюбите его и вы.
              </p>
            </div>
            <div class="cartBtns">
              <div class="cartCounter">
                <button class="counterMinus" @click="cart.quantity--">-</button>
                <div class="number">{{ cart.quantity }}</div>
                <button class="counterPlus" @click="cart.quantity++">+</button>
              </div>
              <button class="add">Добавить</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      carts: [
        {
          id: 1,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#FE724B",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
        {
          id: 2,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#B3E0EB",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
        {
          id: 3,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#FCBEC8",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
        {
          id: 4,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#B3E0EB",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
        {
          id: 5,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#FCBEC8",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
        {
          id: 6,
          title: "Картофель с луком и белыми грибами",
          gramm: "320г",
          kkal: "1040ккал",
          price: "430₽",
          text: "Это вкусное и сытное блюдо является любимым блюдом во многих семьях, полюбите его и вы.",
          imgUrl: "poteto.png",
          bgColor: "#FE724B",
          quantity: 0,
          liked: false,
          heart:
            "M16.5 3C19.538 3 22 5.5 22 9C22 16 14.5 20 12 21.5C9.5 20 2 16 2 9C2 5.5 4.5 3 7.5 3C9.36 3 11 4 12 5C13 4 14.64 3 16.5 3ZM12.934 18.604C13.815 18.048 14.61 17.495 15.354 16.903C18.335 14.533 20 11.943 20 9C20 6.64 18.463 5 16.5 5C15.424 5 14.26 5.57 13.414 6.414L12 7.828L10.586 6.414C9.74 5.57 8.576 5 7.5 5C5.56 5 4 6.656 4 9C4 11.944 5.666 14.533 8.645 16.903C9.39 17.495 10.185 18.048 11.066 18.603C11.365 18.792 11.661 18.973 12 19.175C12.339 18.973 12.635 18.792 12.934 18.604Z",
        },
      ],
    };
  },
  methods: {
    getImage(pic) {
      return require("../assets/content/" + pic);
    },
  },
};
</script>
<style scoped lang="scss">
.container {
  position: relative;
  display: flex;
  flex-direction: column;
  .snaks {
    position: relative;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 40px;
    .title {
      position: absolute;
    }
    .cart {
      position: relative;
      top: 50px;
      width: 355px;
      margin: 20px 0;
      .cartTop {
        height: 360px;
        width: 355px;
        border-radius: 25px 25px 0 0;
        label {
          position: absolute;
          top: 20px;
          left: 20px;

          input {
            position: absolute;
            visibility: hidden;
          }
          .path {
            position: relative;

            svg {
              position: relative;
              width: 25px;
              height: 25px;

              path {
                position: relative;
                transition: 0.2s;

                &.like {
                  fill: #fff;
                }
              }
            }
          }
        }
      }
      .Info {
        position: relative;
        height: 280px;
        width: 355px;
        background: #ffffff80;
        border: 1px solid #ffffff80;
        border-radius: 0 0 25px 0;

        .cartInfo {
          .cartText {
            padding: 10px;
            height: 80px;
            width: 330px;
            font-size: 17px;
            font-weight: 300;
            line-height: 20px;
            text-align: left;
            color: #21262999;
          }
          .infoList {
            list-style: none;
            display: flex;

            .price {
              font-size: 14px;
              font-weight: 700;
              line-height: 20px;
              letter-spacing: 0em;
              text-align: left;
              color: #21262980;
            }
            .listItem {
              list-style: none;
              padding: 10px 20px 0 10px;

              font-size: 14px;
              line-height: 20px;
              letter-spacing: 0em;
              text-align: left;
            }
          }
        }
        .cartTitle {
          padding: 20px 10px 20px 10px;
          height: 70px;
          width: 320px;
          font-size: 20px;
          font-weight: 700;
          line-height: 25px;
          color: #212629;
        }
        .cartCounter {
          height: 40px;
          width: 120px;
          border: 1px solid #ffffff;
          border-radius: 99px;
          display: flex;
          justify-content: space-between;
          align-items: center;
          .number {
            font-size: 18px;
            font-weight: 700;
            line-height: 20px;
            letter-spacing: 0em;
            text-align: left;
            color: #212629;
          }
        }
        button {
          width: 33%;
          border: none;
          background: none;
          font-size: 20px;
        }
        .cartBtns {
          position: absolute;
          bottom: 10px;
          display: flex;
          justify-content: space-between;
          align-items: center;
          margin: 10px;

          .add {
            height: 40px;
            width: 200px;
            border: none;
            border-radius: 99px;
            background: #e9e9e9;
            box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.08),
              -1px -1px 6px rgba(255, 255, 255, 0.5), -5px -5px 20px #ffffff,
              5px 5px 20px #d3d3d3;
            border-radius: 99px;
            color: #fe9102;
            font-size: 18px;
            font-weight: 700;
            line-height: 20px;
            letter-spacing: 0em;
          }
        }
      }
    }
  }
}
</style>
