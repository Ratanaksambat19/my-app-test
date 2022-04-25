<template>
  <div class="card-container">
    <h1>{{name}}</h1>
    <p>{{email}}</p>
    <p>{{phone}}</p>
    <small>{{address.city}}</small>
  </div>
</template>

<script>
export default {
  name: 'UserCard',
  props: ['name', 'email', 'phone', 'address']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card-container {
  border: 1px solid yellow;
  width: 200px;
}
</style>
