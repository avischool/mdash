<template>
  <div id="sector1">
    <h1>Blah</h1>
    <apexchart
      width="170%"
      height="100%"
      type="bar"
      :options="chartOptions"
      :series="series"
    />
    <!-- <h1>{{ bardata }}</h1> -->
  </div>
</template>

<script>
export default {
  name: "chart1",
  data: function () {
    return {
      chartOptions: {
        chart: {
          id: "vuechart-example",
        },
        xaxis: {
          categories: [
            "January",
            "February",
            "March",
            "April",
            "May",
            "June",
            "July",
            "August",
            "September",
            "October",
            "November",
            "December",
          ],
        },
      },
      series: [
        {
          name: "series-1",
          data: [289, 394, 302, 140, 125, 500, 322, 190, 230, 310, 342, 100], //this.$props.bardata, //error is here
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
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
#sector1 {
  display: flex;
}
</style>
