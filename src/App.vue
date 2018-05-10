<template>
  <div id="app">
  	<CartModal/>
  </div>
</template>

<script>
import CartModal from '@/components/CartModal'

export default {
  name: 'App',
  components: {
    CartModal
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
