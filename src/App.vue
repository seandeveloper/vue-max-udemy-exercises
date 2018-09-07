<template>
  <div id="app">
  <section class="header">
   <img width="50%" :src="logo">
   <h1>Max's Udemy Complete Vue Course</h1>
   <h4>Student: Sean Knowles</h4>
   <h5>Exercise and VueJS examples from the Udemy course</h5>
  </section>
  
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
     <ConditionalsVif/><hr>
     <RenderListsVfor/><hr>
     <Exercise5/>
    </div>
    
    
  </div>
</template>

<script>
// Section 2
import WatchersComp from "./components/section2/WatchersComp";
import ShortHand from "./components/section2/25_ShortHand";
import Exercise2 from "./components/section2/Exercise2";
import CssBasics from "./components/section2/26_CssBasics";
import Exercise4 from "./components/section2/Exercise4";

// Section 3
import ConditionalsVif from "./components/section3/ConditionalsVif";
import RenderListsVfor from "./components/section3/RenderListsVfor";
import Exercise5 from "./components/section3/Exercise5";

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
    ConditionalsVif,
    RenderListsVfor,
    Exercise5
  },
  data() {
    return {
      showS2: true,
      showS3: true,
      logo:
        "https://uploads.codesandbox.io/uploads/user/3a8d0d65-9ac0-4303-9d89-08b9ad0f6935/Qy43-vuejs-tutorial.png"
    };
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
