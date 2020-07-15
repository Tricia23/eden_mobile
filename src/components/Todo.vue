
<template>
  <div class="todo">
    <div class="todo__item">
      <div class="todo__day">
        <span>Tomorrow</span>
      </div>
      <div class="todo__wrap">
        <div class="todo__time">
          <span>9 - 10am</span>
        </div>
        <div class="todo__action">
          <span>Your cleaner is coming in to give your apartment the looks.</span>
        </div>
      </div>
    </div>
    <div class="todo__item">
      <div class="todo__day">
        <span>Friday July 27th</span>
      </div>
      <div class="todo__wrap">
        <div class="todo__time">
          <span>9 - 10am</span>
        </div>
        <div class="todo__action">
          <span>Your cleaner is coming in to give your apartment the looks.</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Serif:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");
.todo {
  margin-top: 2rem;
  padding: 1rem 0 7rem 0;
  display: block;
}
.todo__day span {
  color: #00c267;
  font-family: "PT Serif";
  font-size: 17px;
  line-height: 22px;
  display: block;
  text-align: left;
}

.todo__wrap {
  display: flex;
  margin-top: 1rem;
}
.todo__time span {
  font-size: 12px;
  line-height: 15px;
  text-align: left;
  display: block;
  color: #333;
}

.todo__time {
  width: 20%;
  display: flex;
  align-items: center;
}

.todo__action {
  border-radius: 10px;
  background-color: #cfecff80;
  margin-left: 10px;
  padding: 15px;
  width: 80%;
}

.todo__action span {
  color: #121212;
  font-size: 15px;
  font-weight: 300;
  line-height: 19px;
  text-align: left;
  display: block;
}

.todo__item {
  margin-bottom: 1.5rem;
}
</style>