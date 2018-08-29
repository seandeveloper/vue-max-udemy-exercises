<template>
  <div class="hello">
  <h2>Section 2</h2>
    <button @click="counter++">Increase</button>
    <button @click="counter--">Decrease</button>
    <button @click="secondCounter++">Increase Second</button>
    <p>Counter: {{ counter }} | Second {{ secondCounter }}</p>
    <p>{{ countMessage() }} | {{ output }}</p>
  </div>
</template>

<script>
export default {
  name: "WatchersComp",
  data() {
    return {
      counter: 0,
      secondCounter: 0
    };
  },
  computed: {
    output() {
      console.log('Computed')
       return this.counter > 5 ? 'Greater than 5' : 'Less than 5';
    }
  },
  watch: {
    counter (value) {
      let vm = this;
      setTimeout(function() {
        vm.counter = 0;
      }, 2000)
    }
  },
  methods: {
    countMessage() {
      console.log('Method')
      return this.counter > 5 ? 'Greater than 5' : 'Less than 5';
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



</style>
