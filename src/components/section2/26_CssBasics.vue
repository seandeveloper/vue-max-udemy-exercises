<template>
  <div>
    <div @click="attachRed = !attachRed" class="demo" :class="divClasses"></div>
    <div class="demo" :class="color"></div>
    <div class="demo" :style="myStyle"></div>
    <div class="demo" :style="[myStyle, {height: width + 'px'}]"></div>
    <br>
    <input type="text" v-model="color">
    <input type="text" v-model="width">
  </div>
</template>

<script>
export default {
  name: "CssBasics",
  data() {
    return {
      attachRed: false,
      color: "green",
      width: 50
    };
  },
  computed: {
    divClasses() {
      return {
        red: this.attachRed,
        blue: !this.attachRed
      };
    },
    myStyle() {
      return {
        backgroundColor: this.color,
        width: this.width + "px"
      };
    }
  }
};
</script>

<style>
.demo {
  width: 100px;
  height: 100px;
  background-color: grey;
  display: inline-block;
  margin: 10px;
}

.red {
  background-color: red;
}

.blue {
  background-color: blue;
}
.green {
  background-color: green;
}

.yellow {
  background-color: yellow;
}
</style>
