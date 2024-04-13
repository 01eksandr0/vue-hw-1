<template>
  <div>
    <table class="table">
      <thead class="head">
        <tr class="tr">
          <th class="th">Type</th>
          <th class="th">Amount</th>
          <th class="th">Currency</th>
        </tr>
      </thead>
      <tbody class="body">
        <tr v-for="item in list" class="tr" :key="item.id">
          <td class="th">{{ item.type }}</td>
          <td class="th">{{ item.amount }}</td>
          <td class="th">{{ item.currency }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "tabl-transaction",
  props: {
    list: Array,
  },
};
</script>

<style scoped>
.table {
  border: 1px solid black;
  table-layout: fixed;
  width: 270px;
  border-collapse: collapse;
  background-color: antiquewhite;
}
.head {
  background-color: rgb(33, 42, 42);
  color: aliceblue;
}
.body:nth-child(2n-1) {
  background-color: aqua;
}
.tr {
  height: 30px;
}
.th {
  border: 1px solid black;
  text-align: center;
}
</style>
