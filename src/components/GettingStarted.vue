<template>
  <div class="gettingStarted">
    <div class="gettingStarted__wrap">
      <h3>Getting Started</h3>
      <span>Let’s answer any questions you have left!</span>
      <div class="gettingStarted__media">
        <div class="gettingStarted__call">
          <div class="call__icon">
            <img src="../assets/icons/call.png" />
          </div>
          <span>
            Set up a call with
            your gardener
          </span>
          <div class="media__action">
            <span class="call">Do it</span>
            <img src="../assets/icons/play_forward.png" />
          </div>
        </div>
        <div class="gettingStarted__video">
          <div class="video__icon">
            <img src="../assets/icons/play.png" />
          </div>
          <span>
            Lose yourself to
            this video
          </span>
          <div class="media__action">
            <span class="play">Play</span>
            <img src="../assets/icons/call_forward.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.gettingStarted {
  margin-top: 2rem;
  display: flex;
}
.gettingStarted__wrap {
  height: 248px;
  width: 100%;
  border-radius: 6px;
  background-color: #cfecff80;
  padding: 20px 20px 0 20px;
}

.gettingStarted__wrap h3 {
  text-align: left;
  color: #121212;
  font-family: "PT Serif";
  font-size: 17px;
  font-weight: 700;
  line-height: 20px;
  margin: unset;
  letter-spacing: 0.4;
}

.gettingStarted__wrap span {
  display: block;
  text-align: left;
  color: #383838;
  letter-spacing: 0.5;
  font-size: 14px;
  font-weight: 300;
  line-height: 20px;
  margin-top: 1rem;
}

.gettingStarted__media {
  display: flex;
  margin-top: 2rem;
}

.call__icon {
  height: 40px;
  width: 40px;
  background-color: rgba(190, 164, 255, 0.7);
  box-shadow: 0 10px 20px 0 rgba(0, 0, 0, 0.1);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.gettingStarted__call {
  width: 50%;
  padding-left: 1rem;
  padding-right: 1rem;
}
.gettingStarted__video {
  width: 50%;
  padding-left: 1rem;
  padding-right: 1rem;
}

.gettingStarted__call span {
  display: block;
  color: #383838;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  margin-top: 13px;
  letter-spacing: 0.4;
}
.gettingStarted__video span {
  display: block;
  color: #383838;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  margin-top: 13px;
  letter-spacing: 0.4;
}

.call__icon img {
  height: 17.33px;
  width: 19.39px;
}

.video__icon img {
  height: 14px;
  width: 14px;
}

.video__icon {
  height: 40px;
  width: 40px;
  background-color: rgba(255, 146, 101, 0.7);
  box-shadow: 0 10px 20px 0 rgba(0, 0, 0, 0.1);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.media__action {
  display: flex;
  align-items: center;
  margin-top: 1rem;
}

.media__action span {
  display: inline-block;
}

.media__action img {
  height: 9px;
  width: 14px;
  margin-left: 7px;
}

.media__action .call {
  color: #8a5cff;
  display: block;
  margin: auto 0;
  border-bottom: 1px solid #8a5cff;
  line-height: 13px;
}
.media__action .play {
  color: #ff682a;
  display: block;
  margin: auto 0;
  border-bottom: 1px solid #ff682a;
  line-height: 13px;
}
</style>