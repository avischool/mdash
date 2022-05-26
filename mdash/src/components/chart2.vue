<template>
  <div id="sector2">
    <h1>Patient Ages</h1>
    <div id="chart2">
      <apexchart
        width="150%"
        height="150%"
        type="donut"
        :options="options"
        :series="series"
      ></apexchart>
    </div>
  </div>
</template>

<script>
export default {
  name: "chart2",
  data: function () {
    return {
      options: { labels: ["<8", "8-12", "12-18", "18-21"] },
      series: [44, 55, 41, 17],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
#sector2 {
  margin: 0 auto;
  display: flex;
}

#chart2 {
  display: flex;
}
</style>
