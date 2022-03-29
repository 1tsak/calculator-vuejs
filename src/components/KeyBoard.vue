<template>
  <div class="key-border" style="max-width:450px; margin:auto; background: #234;">
    <div class="row no-gutters">
      <div class="col-3 cbtn" v-for="n in calculatorkeys" :key="n">
        <div class="" @click="emit(n)" style="margin:10px; color:white;">
          {{n}}
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "KeyBoard",
  props: {},
  data(){
    return{
      calculatorkeys:['%','C','/','x',7,8,9,'X',4,5,6,'-',1,2,3,'+','00',0,'.','='],

    }
  },
  methods:{
      emit(a){
          this.$emit('key-press',a);
      }
  }
};
</script>
<style scoped>
.key-border {
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  margin-top: 5px;
}
.row {
  display: flex;
}
.cbtn {
}
.cbtn:hover{
  background: #000;
  cursor: pointer;
}
</style>