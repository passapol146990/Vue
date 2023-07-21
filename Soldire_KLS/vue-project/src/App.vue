<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
// import WelcomeItemVue from './components/WelcomeItem.vue'
import BarVue from './components/Bar.vue'
import MenuVue from "./components/Menu.vue"
import AddmeVue from "./components/Addme.vue"
import ContactVue from "./components/Contact.vue"
</script>

<template>
<div>
  <BarVue/>
  <MenuVue/>
  <AddmeVue/>
  <ContactVue/>
</div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
