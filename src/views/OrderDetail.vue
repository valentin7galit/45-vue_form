<template>
  <div id="order-detail">
    <Form msg="Order Details"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Form from '@/components/Form.vue'

export default {
  name: 'OrderDetail',
  components: {
    Form
  }
}
</script>

<style scoped>
#order-detail {
  margin: auto;
  border: 1px solid #2c3e50;
  border-radius: 5px;
  width: 80%;
  text-align: left;
}
@media (max-width: 960px) {
  #order-detail {
    width: 100%;
  }
}
</style>
