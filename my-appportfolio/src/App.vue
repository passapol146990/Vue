<template>
  <navbar/>
  <slider/>
</template>

<script>
import navbar from './components/navbar.vue'
import slider from './components/slider.vue'

export default {
  name: 'App',
  components: {
    navbar,
    slider,
  }
}
</script>

<style>
#logo{
  margin-top: 7px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-left: 1rem;
  box-shadow: 0 0px 5px #fff;
}
</style>
