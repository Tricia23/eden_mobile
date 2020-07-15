<template>
  <div class="details">
    <div class="schedule__wrap">
      <h2>Schedule</h2>
      <div class="schedule__reconfigure">
        <div class="schedule__reconfigure__text">Reconfigure Services</div>
      </div>
    </div>
    <div class="account__status">
      <div class="account__status-wrap">
        <div class="account__status-label">
          <span>
            Your account is inactive.
            <span class="dark">15% off</span> offer until June 23.
          </span>
        </div>
        <div class="account__status-price">
          <div>
            <span class="main__price">N75,000</span>
            <span class="discount__price">Pay N62,800</span>
          </div>
        </div>
      </div>
    </div>

    <div class="meal__status">
      <a class="meal__status-wrap" :class="{ 'meal__status--active': mealStatusActive }">
        <div class="meal__status-flex" :class="{ 'mealStatusFlexed': mealStatusFlexed}">
          <div
            class="meal__status-label"
            :class="{ 'meal__status--Grow': mealStatusGrow, 'borderL': borderL }"
          >
            <span v-if="!mealTitle" class="view__meal">View your meals for the week.</span>
            <transition name="fadeText">
              <span v-if="mealTitle" class="todays__meal">Today’s Meals</span>
            </transition>
          </div>
          <div
            @click="toggle = !toggle; mealStatusActive = !mealStatusActive; mealStatusGrow = !mealStatusGrow; borderL = !borderL; borderR = !borderR; visible=!visible; mealTitle=!mealTitle; mealStatusFlexed =! mealStatusFlexed; "
            class="account__status-list"
            :class="{ 'meal__status--Grow': mealStatusGrow, 'borderR': borderR }"
          >
            <span v-if="!mealTitle">Check ‘em</span>
            <transition name="fadeText">
              <img v-if="mealTitle" class="close__button" src="../assets/images/close.png" />
            </transition>
          </div>
        </div>
        <div v-if="visible" class="food__menu" :class="{'food__menu-fixed' : foodMenuFixed}">
          <a href="#" class="food__list" v-for="(food, i) in foods" :key="i">
            <div class="food__image">
              <img
                :src="food.image"
                :class="getImageClass(i)"
                @click="onImageClick(i); toggled = !toggled; foodMenuFixed=!foodMenuFixed; "
              />
            </div>
            <div class="food__details">
              <span class="food__name">{{food.name}}</span>
              <span class="food__type">{{food.type}}</span>
            </div>
          </a>
          <transition name="fade">
            <div @click="toggled = !toggled; onImageClick(i);" v-if="toggled" class="overlay"></div>
          </transition>
        </div>
      </a>
    </div>

    <transition name="fade">
      <div v-if="toggle" class="overlay"></div>
    </transition>
  </div>
</template>
<script>
export default {
  data() {
    return {
      toggle: false,
      visible: false,
      mealTitle: false,
      toggled: false,
      foodMenuFixed: false,
      toggledoff: false,
      foodMenuOff: false,
      fullWidthImageIndex: null,
      foods: [
        {
          image: require("../assets/images/food.png"),
          name: "Akara & Pap",
          type: "Carbohydrate"
        },
        {
          image: require("../assets/images/food1.png"),
          name: "Jollof rice",
          type: "Protein"
        },
        {
          image: require("../assets/images/food2.png"),
          name: "Gastonton",
          type: "Carbohydrate"
        },
        {
          image: require("../assets/images/food3.png"),
          name: "Port Domenic",
          type: "Carbohydrate"
        },
        {
          image: require("../assets/images/food4.png"),
          name: "Carleville",
          type: "Fats and Oil"
        },
        {
          image: require("../assets/images/food5.png"),
          name: "South Chesleyton",
          type: "Vegetable"
        },
        {
          image: require("../assets/images/food3.png"),
          name: "Port Domenic",
          type: "Carbohydrate"
        },
        {
          image: require("../assets/images/food4.png"),
          name: "Carleville",
          type: "Fats and Oil"
        },
        {
          image: require("../assets/images/food5.png"),
          name: "South Chesleyton",
          type: "Vegetable"
        }
      ]
    };
  },
  methods: {
    getImageClass: function(i) {
      return {
        fullWidthImage: this.fullWidthImageIndex === i
      };
    },
    onImageClick: function(i) {
      if (this.fullWidthImageIndex === i) {
        this.fullWidthImageIndex = null;
      } else {
        this.fullWidthImageIndex = i;
      }
    }
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Serif:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");
.details {
  margin-top: 2rem;
}
.schedule__wrap {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.schedule__wrap h2 {
  margin: unset;
  height: 37px;
  width: 121px;
  color: #121212;
  font-family: "PT Serif";
  font-size: 28px;
  font-weight: 700;
  line-height: 37px;
  text-align: center;
}
.schedule__reconfigure {
  display: flex;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
  height: 25px;
  width: 140px;
  border-radius: 13px;
  background-color: #ff9d000f;
  border: 0.8px solid #fe9b00;
}

.schedule__reconfigure__text {
  color: #e78f00;
  font-family: "Cerebri Sans";
  font-size: 12px;
  line-height: 15px;
  text-align: center;
}

.account__status {
  margin-top: 1.5rem;
}

.account__status-wrap {
  display: flex;
}
a {
  text-decoration: none;
}
.account__status-label {
  display: flex;
  align-items: center;
  padding: 0 15px;
  height: 64px;
  width: 60%;
  font-size: 14px;
  font-weight: 300;
  line-height: 20px;
  border-radius: 6px 0 0 6px;
  background-color: #00c2671a;
}

.account__status-label span {
  color: #1b1b1b;
  font-size: 14px;
  font-weight: 300;
  text-align: left;
  line-height: 20px;
  display: inline-block;
}

.account__status-label .dark {
  font-weight: 600;
  display: inline-block;
}
.account__status-price {
  height: 64px;
  width: 40%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0 6px 6px 0;
  background-color: #00c267;
}

.main__price {
  display: block;

  text-decoration: line-through;
  color: #fff;

  font-size: 14px;
  line-height: 17px;
  font-family: sans-serif;
  letter-spacing: 0.4px;
}

.discount__price {
  display: block;
  color: #fff;
  font-size: 14px;
  font-weight: 600;
  line-height: 17px;
  margin-top: 4px;

  letter-spacing: 0.4px;
}

.meal__status {
  margin-top: 1.5rem;
  position: relative;
  z-index: 99999;
}

.meal__status-wrap {
  display: block;
}
.meal__status-flex {
  display: flex;
  transition-duration: 1s;
  transition-timing-function: ease;
}
.mealStatusFlexed {
  display: flex;
  position: fixed;
  width: 100%;
  transition-duration: 1s;
  transition-timing-function: ease;
}

.close__button {
  position: absolute;
  display: block;
  height: 25px;
  width: 25px;
}

.meal__status-label {
  display: flex;
  align-items: center;
  padding: 0 15px;
  height: 64px;
  width: 60%;
  font-size: 14px;
  font-weight: 300;
  border-radius: 6px 0 0 6px;
  background-color: #f9f5e1;
  z-index: 999999;
  transition-duration: 1s;
  transition-timing-function: ease;
}

.meal__status-label span {
  color: #1b1b1b;
  font-size: 14px;
  font-weight: 300;
  text-align: left;
  line-height: 19px;
  display: inline-block;
  display: block;
  top: 30%;
  font-family: sans-serif;
  letter-spacing: 0.4px;
}

.meal__status-label .todays__meal {
  color: #121212;
  font-size: 20px;
  font-weight: 700;
  line-height: 26px;
  margin-left: 10px;
  position: absolute;
  font-family: "PT Serif";
}

.account__status-list {
  height: 64px;
  width: 40%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0 6px 6px 0;
  background-color: #ffbe56;
  z-index: 999999;
  transition-duration: 1s;
  transition-timing-function: ease;
}

.account__status-list span {
  display: block;
  color: #fff;

  letter-spacing: 0.4px;
  font-size: 14px;
  line-height: 17px;
  background-color: #ffbe56;
  font-weight: 600;
}

.overlay {
  background: rgba(0, 0, 0, 0.9);
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: block;
  text-align: center;
  transition: opacity 500ms;
  opacity: 1;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-to,
.fade-leave {
  opacity: 1;
}

.fadeText-enter-active,
.fadeText-leave-active {
  transition: opacity 0.2s linear;
}

.fadeText-enter,
.fadeText-leave-to {
  opacity: 0;
}

.fadeText-enter-to,
.fadeText-leave {
  opacity: 1;
}

.meal__status--active {
  position: fixed;
  left: 0;
  margin-top: -165px;
  width: 100vw;
  transition-duration: 1s;
  transition-timing-function: ease;
  height: 100vh;
  background-color: #ffffff;
  border-radius: 20px;
  overflow-y: scroll;
}

.meal__status--Grow {
  height: 87px;
  transition-duration: 1s;
}
.meal__status--Grow {
  height: 87px;
  transition-duration: 1s;
}
.borderL {
  border-radius: 20px 0 0 0;
  transition-duration: 1s;
}

.fullWidthImage {
  width: 100vw !important;
  height: 450px !important;
  display: flex;
  position: absolute;
  z-index: 999999;
  left: 0;
  top: 8%;
  transition-duration: 1s;
  transition-timing-function: ease;
  border-radius: 0 !important;
}
.toggledoff {
  display: none;
}

.borderR {
  border-radius: 0 20px 0 0;
  transition-duration: 1s;
}
.food__menu {
  padding: 7.5rem 0 6rem 2rem;
}

.food__menu-fixed {
  position: fixed;
}
.food__list {
  display: flex;
  margin-bottom: 2rem;
  display: flex;
  align-items: center;
}
.food__name {
  color: #303030;
  font-size: 18px;
  font-weight: 300;
  line-height: 24px;
  display: block;
  text-align: left;
}
.food__type {
  color: #6c6c6c;
  font-size: 15px;
  font-weight: 300;
  line-height: 24px;
  display: block;
  text-align: left;
}

.food__details {
  margin-left: 20px;
}
.food__image {
  height: 60px;
  width: 60px;
}

.food__image img {
  height: 60px;
  width: 60px;
  transition-duration: 1s;
  transition-timing-function: ease;
  border-radius: 10px;
}

.foodMenuOff {
  display: none;
}

.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
</style>