<template>
  <CenterWindow />
</template>

<script>
import CenterWindow from './components/CenterWindow.vue'
import './assets/css/variables.css'

export default {
  components: {
    CenterWindow
  },
  data() {
    return {
      isDarkMode: JSON.parse(localStorage.getItem('darkMode')) || false
    }
  }
}
</script>

<style>
.dark-mode {
  background-color: #333;
  color: #fff;
}
</style>
