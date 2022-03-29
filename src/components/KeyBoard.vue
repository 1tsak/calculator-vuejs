<template>
  <div class="display-border">
    <div class="row row1">
      <button class="cbtn" @click="this.emit('C')">C</button>
      <button class="cbtn" @click="this.emit('X')">X</button>
      <button class="cbtn" @click="this.emit('%')">%</button>
      <button class="cbtn" @click="this.emit('/')">/</button>
    </div>
    <div class="row row2">
      <button class="cbtn" @click="this.emit('x')">x</button>
      <button class="cbtn" @click="this.emit('9')">9</button>
      <button class="cbtn" @click="this.emit('8')">8</button>
      <button class="cbtn" @click="this.emit('7')">7</button>
    </div>
    <div class="row row3">
      <button class="cbtn" @click="this.emit('-')">-</button>
      <button class="cbtn" @click="this.emit('6')">6</button>
      <button class="cbtn" @click="this.emit('5')">5</button>
      <button class="cbtn" @click="this.emit('4')">4</button>
    </div>
    <div class="row row4">
      <button class="cbtn" @click="this.emit('+')">+</button>
      <button class="cbtn" @click="this.emit('3')">3</button>
      <button class="cbtn" @click="this.emit('2')">2</button>
      <button class="cbtn" @click="this.emit('1')">1</button>
    </div>
    <div class="row row5">
      <button class="cbtn" @click="this.emit('=')">=</button>
      <button class="cbtn" @click="this.emit('.')">.</button>
      <button class="cbtn" @click="this.emit('0')">0</button>
      <button class="cbtn" @click="this.emit('00')">00</button>
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
.cbtn:hover{
  background: #000;
}
</style>