<template>
  <div id="app">
    <h1>Welcome to MDash</h1>
    <h3>Add your updated report here</h3>
    <h3>{{ bardata }}</h3>
    <fileupload />
    <div id="container">
      <carousel :items-to-show="1">
        <slide :key="1"> <chart /> </slide>
        <slide :key="2"> <chart2 /> </slide>
        <slide :key="3"> <table1 /> </slide>

        <template #addons>
          <navigation />
          <pagination />
        </template>
      </carousel>
    </div>
    <!-- <h1 style="font-size:300%">Hey ____!</h1> -->
    <!-- <clock /> -->
  </div>
</template>

<script>
import chart from "./components/chart1.vue";
import chart2 from "./components/chart2.vue";
import fileupload from "./components/fileupload.vue";
import table1 from "./components/table1.vue";

import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

export default {
  name: "App",
  components: {
    chart,
    chart2,
    fileupload,
    table1,
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  props: ["bardata"],
  // data: function () {
  //   return { child_component: "table1" };
  // },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
}

#container {
  display: flex;
  flex-flow: row;
  justify-content: center;
}

// #sector1,
// #sector2,
// #sector3 {
//   margin: 0 auto;
//   width: 27em;
//   align-content: center;
//   display: flex;
//   flex-flow: column;
//   justify-content: center;
//   margin-top: 10px;
//   text-align: center;
// }
</style>
