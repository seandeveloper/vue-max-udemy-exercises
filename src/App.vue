<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <br>
    <!-- Menu buttons -->
    <button @click="showS2 = !showS2">Section 2</button>
    <button @click="showS3 = !showS3">Section 3</button>

    <!-- SECTION 2 -->
    <div v-if="!showS2">
      <h3>Section2</h3>
      <WatchersComp/><hr>
      <ShortHand/><hr>
      <Exercise2/><hr>
      <CssBasics/><hr>
      <h3>Section 4</h3>
      <!--<Exercise4/>--><hr> <!--TODO: Excercise not finished -->
    </div>

    <!-- SECTION 3 -->
    <div v-if="showS3">
     <h3>Section3</h3>
     <ConditionalsVif/>
    </div>
    
    
  </div>
</template>

<script>
// Section 2
import WatchersComp from "./components/section2/WatchersComp";
import ShortHand from './components/section2/25_ShortHand'
import Exercise2 from './components/section2/Exercise2'
import CssBasics from './components/section2/26_CssBasics'
import Exercise4 from './components/section2/Exercise4'

// Section 3
import ConditionalsVif from './components/section3/ConditionalsVif'

export default {
  name: "App",
  components: {
    //section 2
    WatchersComp,
    ShortHand,
    Exercise2,
    CssBasics,
    Exercise4,
    //section 3
    ConditionalsVif
  },
  data() {
    return {
      showS2: true,
      showS3: true
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
hr {
  margin: 50px;
}

button {
  margin: 2px;
}
</style>
