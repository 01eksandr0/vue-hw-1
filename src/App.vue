<template>
  <div class="container">
    <user-cart :cart="user"></user-cart>
    <ul style="display: flex; gap: 10px">
      <li v-for="friend in friends" :key="friend.id">
        <friend :friend="friend" />
      </li>
    </ul>

    <Transation :list="table"></Transation>
  </div>
</template>

<script>
import UserCart from "./components/UserCart.vue";
import Friend from "./components/Friend.vue";
import user from "./DATA/user.json";
import friends from "./DATA/friends.json";
import table from "./DATA/table.json";
import Transation from "./components/Transaction.vue";
export default {
  name: "App",
  components: { UserCart, Friend, Transation },
  data() {
    return {
      user,
      friends,
      table,
    };
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
li {
  list-style: none;
}
.container {
  padding: 20px;
  background-color: #fafafa;
  display: flex;
  gap: 20px;
}
</style>
