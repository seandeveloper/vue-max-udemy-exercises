<template>
  <div>
  <h4>Conditionals v-if</h4>
  <p v-if="show">You can see me!</p>
  <p v-else>Do you also see me</p>
  <button @click="show = !show">Click me</button>
  </div>
</template>

<script>
export default {
  name: "ConditionalsVif",
  data() {
    return {
      show: true
    };
  }
};
</script>

<style>
</style>
