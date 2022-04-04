<template>
  <h1 style=" margin:10px;font-family:monospace">Calculator</h1>
  <DisplayScreen :output="this.output" />
  <KeyBoard @key-press="updateScreen" />
  <div class="footer m-lg-3">
    
  <a href="https://instagram.com/1ts.akash" ><img class="social-ic" src="./assets/instagram-light.svg" alt="insta"></a>
  <a href="https://github.com/1tsak" ><img class="social-ic" src="./assets/github-light.svg" alt="github"></a>
  <a href="https://youtube.com/AKBROS" ><img class="social-ic" src="./assets/youtube-light.svg" alt="yt"></a>
  <p style="margin-top:25px;">Made With💖 by 1tsak</p></div>
</template>

<script>
import DisplayScreen from "./components/DisplayScreen.vue";
import KeyBoard from "./components/KeyBoard.vue";

export default {
  name: "App",
  components: {
    DisplayScreen,
    KeyBoard,
  },
  data() {
    return {
      output: "0",
      calval:'0',
      operator: null,
      preCalVal: "",
    };
  },
  methods: {
    updateScreen(output) {
      /* Append Value */
      if (!isNaN(output) || output === ".") {
        if (this.calval === "0") {
          console.log("c1");

          this.output = output;
          this.calval = output;
        } else {
          this.output += output;
          this.calval +=output;

          console.log("c2");
        }
      }
      
      /* Clear Value */
      if (output === "C") {
        this.output = "0";
        this.preCalVal='0'
        this.operator=null;
        this.calval='0'
      }
      
      /* Percentage */
      if (output === "%") {
        this.output = this.output / 100 + "";
        this.calval=this.output/100+'';
      }
      
      /* Append Value */
      if(['+','-','*','/'].includes(output)){
        this.operator = output;
        this.preCalVal=this.calval
        this.output=this.preCalVal+this.operator;
        this.calval=this.preCalVal+this.operator;
      }
      if(output==='='){
        this.output= eval(this.calval);
        this.preCalVal='';
        this.operator=null;
      }
    },
  },
};
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
.social-ic{
  margin: 8px;
}
.social-ic:hover{
  cursor: pointer;
  box-shadow: 0px 1px 0px 2px rgba(0, 0, 0, 0.259);
}
</style>
