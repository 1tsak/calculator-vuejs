<template>
<h1>Calculator</h1>
<DisplayScreen :output="0"/>
<KeyBoard/>
</template>

<script>
import DisplayScreen from './components/DisplayScreen.vue'
import KeyBoard from './components/KeyBoard.vue'

export default {
  name: 'App',
  components: {
    DisplayScreen,
    KeyBoard
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
</style>
