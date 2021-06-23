<template>
  <div id="app">
    <OrderDetail msg="Order Details"/>
  </div>
</template>

<script>
import OrderDetail from './components/OrderDetail.vue'

export default {
  name: 'App',
  components: {
    OrderDetail
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: auto;
  margin-top: 15px;
  border: 1px solid #2c3e50;
  border-radius: 5px;
  width: 80%;
}
@media (max-width: 960px) {
  #app {
    width: 100%;
  }
}
</style>
