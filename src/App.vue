<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="card-container" v-for="data in info.data" v-bind:key="data.name">
      <UserCard 
      :name="data.name"
      :email="data.email"
      :phone="data.phone"
      :address="data.address"
      />
    </div>
  </div>
</template>

<script>
import UserCard from './components/UserCard.vue'
import axios from 'axios'

export default {
  name: 'App',
  data () {
    return {
      info: null
    }
  },
  components: {
    UserCard
  },
  mounted () {
    axios
      .get('https://jsonplaceholder.typicode.com/users')
      .then(response => (this.info = response))
  },
  computed: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.card-container {

}
</style>
