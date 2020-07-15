<template>
  <div class="user">
    <div class="user__wrap">
      <div class="user__avatar">
        <div class="user__image"></div>
      </div>
      <div class="user__name">Good Morning Silm!</div>
    </div>
  </div>
</template>


<style scoped>
.user__wrap {
  display: flex;
  align-items: center;
}

.user__avatar {
  height: 35px;
  width: 35px;
  border-radius: 50%;
  background-color: #ffb48f;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}
.user__image {
  height: 31px;
  width: 31px;
  border-radius: 50%;
  background-color: #ffb48f;
  background: url("../assets/images/avatar.png");
  background-position: top;
  background-size: contain;
  background-repeat: no-repeat;
}

.user__avatar img {
  height: 31px;
  width: 31px;
}
.user__name {
  height: 22px;
  width: 153px;
  color: #121212;
  font-family: "PT Serif";
  font-size: 17px;
  line-height: 22px;
  text-transform: capitalize;
  margin-left: 15px;
}
</style>