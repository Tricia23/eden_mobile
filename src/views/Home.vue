<template>
  <div class="home">
    <UserProfile />
    <AccountDetails />
    <GettingStarted />
    <Todo />
    <BottomNav />
  </div>
</template>

<script>
// @ is an alias to /src
import UserProfile from "@/components/UserProfile.vue";
import AccountDetails from "@/components/AccountDetails.vue";
import GettingStarted from "@/components/GettingStarted.vue";
import BottomNav from "@/components/BottomNav.vue";
import Todo from "@/components/Todo.vue";

export default {
  name: "Home",
  components: {
    UserProfile,
    AccountDetails,
    GettingStarted,
    BottomNav,
    Todo
  }
};
</script>

<style scoped>
.home {
  width: 90%;
  display: block;
  margin: auto;
  padding-top: 15px;
  overflow-y: scroll;
}
</style>