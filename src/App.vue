<template>
  <div id="app">
   <MyHeader></MyHeader>
   <router-view></router-view>
   <Footer v-show="$route.meta.show"></Footer>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader'
import Footer from './components/Footer'
export default {
  name: 'App',
  components: {MyHeader,Footer}
}
</script>

<style>

</style>
