<template>
  <div class="item">
    <img width="60" height="60" :src="friend.avatar" alt="" />
    <h2>{{ friend.name }}</h2>
    <p class="online" v-if="friend.isOnline">Online</p>
    <p class="offline" v-else>Offline</p>
  </div>
</template>

<script>
export default {
  name: "friend",
  props: {
    friend: { type: Object },
  },
};
</script>

<style scoped>
.item {
  display: flex;
  padding: 20px;
  flex-direction: column;
  gap: 20px;
  align-items: center;
  background-color: cornsilk;
  border-radius: 10px;
}
.online {
  font-size: 18px;
  color: green;
}
.offline {
  font-size: 18px;
  color: red;
}
</style>
