<template>
<h1>Calculator</h1>
<DisplayScreen :output="this.output"/>
<KeyBoard @key-press="updateScreen"/>
</template>

<script>
import DisplayScreen from './components/DisplayScreen.vue'
import KeyBoard from './components/KeyBoard.vue'

export default {
  name: 'App',
  components: {
    DisplayScreen,
    KeyBoard
  },
  data(){
    return {
      output:"abcd"

      }

    }
  ,
  methods:{
        updateScreen(output){
            this.output=output
            // DisplayScreen.
        }
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
