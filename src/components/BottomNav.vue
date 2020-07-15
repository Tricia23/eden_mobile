<template>
  <div>
    <div class="bottom-navbar">
      <a href="#">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g id="insert_invitation_24px">
            <path
              id="icon"
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M18 4H19C20.1 4 21 4.9 21 6V20C21 21.1 20.1 22 19 22H5C3.89 22 3 21.1 3 20L3.01 6C3.01 4.9 3.89 4 5 4H6V2H8V4H16V2H18V4ZM5 10V20H19V10H5ZM19 8H5V6H19V8ZM12 13H17V18H12V13Z"
              fill="#888DA6"
            />
          </g>
        </svg>
        <span>Schedule</span>
      </a>
      <a href="#">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 20"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            id="icon"
            opacity="0.9"
            d="M13.7086 0C8.02286 0 3.42857 4.47778 3.42857 10H0L4.45143 14.3278L4.53143 14.4889L9.14286 10H5.71429C5.71429 5.70556 9.29714 2.22222 13.7143 2.22222C18.1314 2.22222 21.7143 5.70556 21.7143 10C21.7143 14.2944 18.1314 17.7778 13.7143 17.7778C11.5029 17.7778 9.50857 16.9 8.06286 15.4944L6.44571 17.0667C8.30286 18.8778 10.8686 20 13.7086 20C19.3943 20 24 15.5222 24 10C24 4.47778 19.3943 0 13.7086 0ZM12.5714 5.55556V11.1111L17.4629 13.9333L18.2857 12.5833L14.2857 10.2778V5.55556H12.5714Z"
            fill="#888DA6"
          />
        </svg>
        <span>History</span>
      </a>
      <a href="#">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g id="alert/notification_important_24px">
            <path
              id="icon"
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M10.5 2.75C10.5 1.92 11.17 1.25 12 1.25C12.83 1.25 13.5 1.92 13.5 2.75V3.92C16.64 4.6 19 7.4 19 10.75V16.75L21 18.75V19.75H3V18.75L5 16.75V10.75C5 7.4 7.36 4.6 10.5 3.92V2.75ZM12 5.75C14.76 5.75 17 7.99 17 10.75V17.75H7V10.75C7 7.99 9.24 5.75 12 5.75ZM10.01 20.76C10.01 21.86 10.9 22.75 12 22.75C13.1 22.75 13.99 21.86 13.99 20.76H10.01Z"
              fill="#888DA6"
            />
          </g>
        </svg>
        <span>Notification</span>
      </a>
      <a xlink:href="#">
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g id="chat_24px">
            <path
              id="icon"
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M2.01 4C2.01 2.9 2.9 2 4 2H20C21.1 2 22 2.9 22 4V16C22 17.1 21.1 18 20 18H6L2 22L2.01 4ZM20 4H4V17.17L5.17 16H20V4ZM6 11H14V13H6V11ZM18 7H6V9H18V7Z"
              fill="#888DA6"
            />
          </g>
        </svg>
        <span>Chat</span>
      </a>
    </div>
  </div>
</template>



<script>
export default {
  data() {
    return {
      date: false,
      chat: false,
      bell: false,
      history: false
    };
  }
};
</script>




<style scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Serif:wght@400;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");
.bottom-navbar {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0.8rem 2rem 2rem 2rem;
  background-color: rgba(244, 244, 244, 0.75);

  justify-content: space-between;
}

.bottom-navbar a {
  text-decoration: none;
}

a #icon:active {
  fill: #00c267;
}

.bottom-navbar span {
  display: block;
  color: #303030;
  font-size: 12px;
  font-weight: 300;
  line-height: 22px;
}
</style>