<template>
  <div class="display-border">
    <div class="row row1">
      <button class="cbtn" @click="emit('C')">C</button>
      <button class="cbtn">X</button>
      <button class="cbtn">%</button>
      <button class="cbtn">/</button>
    </div>
    <div class="row row2">
      <button class="cbtn">x</button>
      <button class="cbtn">9</button>
      <button class="cbtn">8</button>
      <button class="cbtn">7</button>
    </div>
    <div class="row row3">
      <button class="cbtn">-</button>
      <button class="cbtn">6</button>
      <button class="cbtn">5</button>
      <button class="cbtn">4</button>
    </div>
    <div class="row row4">
      <button class="cbtn">+</button>
      <button class="cbtn">3</button>
      <button class="cbtn">2</button>
      <button class="cbtn">1</button>
    </div>
    <div class="row row5">
      <button class="cbtn">=</button>
      <button class="cbtn">.</button>
      <button class="cbtn">0</button>
      <button class="cbtn">00</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "KeyBoard",
  props: {},
  methods:{
      emit(a){
          this.$emit('key-press',a);
      }
  }
};
</script>
<style scoped>
.display-border {
  border: 1px solid black;
  border-radius: 5px;
  margin-top: 5px;
}
.row {
  display: flex;
}
.cbtn {
  flex: 1;
  height: 50px;
  border: none;
  color: white;
  font-size: 18px;
  background: rgba(0, 0, 0, 0.363);
}
</style>