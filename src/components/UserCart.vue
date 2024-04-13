<template>
  <div class="item">
    <div class="img-container">
      <img :src="cart.avatar" alt="" height="40" width="40" />
      <p>{{ cart.username }}</p>
      <p>{{ cart.tag }}</p>
      <p>{{ cart.location }}</p>
    </div>
    <div class="info">
      <div class="sot">
        <p>Followers</p>
        <p>{{ cart.stats.followers }}</p>
      </div>
      <div class="sot">
        <p>Views</p>
        <p>{{ cart.stats.views }}</p>
      </div>
      <div class="sot">
        <p>Likes</p>
        <p>{{ cart.stats.likes }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "user-cart",
  props: {
    cart: {
      type: Object,
    },
  },
};
</script>

<style scoped>
.item {
  border-radius: 10px;
  background-color: rgb(190, 190, 190);
  height: 200px;
}
.img-container {
  display: flex;
  flex-direction: column;
  gap: 7px;
  align-items: center;
  justify-content: start;
  padding: 20px;
}
.info {
  display: flex;
  gap: 5px;
  background: rgb(90, 90, 90);
  padding: 20px;
}
</style>
