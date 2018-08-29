<template>
<div>
<button @click="changeLink">Change Link</button>
<br>
<p>
  {{link}}
</p>
</div>
</template>

<script>
export default {
  name: "ShortHand",
  data() {
    return {
      link: "http://google.com"
    };
  },
  methods: {
    changeLink() {
      this.link = "http://apple.com";
    }
  }
};
</script>

<style scoped>
</style>
