<template>
  <div>
  <h3>Exercise4</h3>
  <!-- 1) Start the Effect with the Button. 
  The Effect should alternate the "highlight" 
  or "shrink" class on each new setInterval tick 
  (attach respective class to the div with id "effect" below) -->
  <div>
    <button @click="startEffect">Start Effect</button>
    <div id="effect"></div>
  </div>
  <!-- 2) Create a couple of CSS classes and
   attach them via the array syntax -->
  <div :style="['float', 'blue', 'text-color']">I got no class :(</div>
  <!-- 3) Let the user enter a class (create 
  some example classes) and attach it -->
  <div>
    <input type="text">
    <div></div>
  </div>
  <!-- 4) Let the user enter a class and enter 
  true/ false for another class (create some example classes)
   and attach the classes -->
  <div>
    <input type="text">
    <input type="text">
    <div></div>
  </div>
  <!-- 5) Repeat 3) but now with values for styles 
  (instead of class names). Attach the respective styles.  -->
  <div>
    <input type="text">
    <div></div>
  </div>
  <!-- 6) Create a simple progress bar with setInterval and style bindings. 
  Start it by hitting the below button. -->
  <div>
    <button v-on:click="startProgress">Start Progress</button>
    <div></div>
  </div>
  </div>
</template>

<script>
export default {
  name: "Exercise4",
  data() {
    return {
      colorOne: "red"
    };
  },
  computed: {
    sideEffect() {
      return {};
    }
  },
  methods: {}
};
</script>

<style scoped>
div {
  margin: 10px;
}

input {
  margin-left: 5px;
}

.float {
  float: right;
}

.blue {
  background-color: blue;
}

.text-color {
  color: yellow;
}
</style>
