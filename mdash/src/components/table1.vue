<template>
  <div id="sector3">
    <h1>Missed Appointments</h1>
    <div id="table1">
      <table class="rwd-table">
        <thead>
          <tr>
            <th>Last Visit</th>
            <th>Next visit</th>
            <th>Age</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="row in rows" :key="row.patient_id">
            <!-- <td data-title="id">{{ product.id }}</td> -->
            <!-- <td><img v-bind:src="product.image" /></td> -->
            <td data-title="last_vist">{{ row.last_visit }}</td>
            <td data-title="next_visit">{{ row.next_visit }}</td>
            <td data-title="age">{{ row.patient_age }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "table1",
  data: function () {
    return {
      rows: [
        {
          patient_id: 45,
          last_visit: "10-05-17",
          next_visit: "17-05-17",
          patient_age: 0.2,
        },
        {
          patient_id: 293,
          last_visit: "9-05-16",
          next_visit: "9-05-17",
          patient_age: 5,
        },
        {
          patient_id: 45,
          last_visit: "10-05-17",
          next_visit: "17-05-17",
          patient_age: 0.2,
        },
        {
          patient_id: 45,
          last_visit: "10-05-17",
          next_visit: "17-05-17",
          patient_age: 0.2,
        },
        {
          patient_id: 45,
          last_visit: "10-05-17",
          next_visit: "17-05-17",
          patient_age: 0.2,
        },
        {
          patient_id: 45,
          last_visit: "10-05-17",
          next_visit: "17-05-17",
          patient_age: 0.2,
        },
      ],
    };
  },
};
</script>

<style>
.rwd-table {
  margin: 1em 0;
  min-width: 300px;
}

tr {
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
}

th {
}

body {
  font-family: Montserrat, sans-serif;
  -webkit-font-smoothing: antialiased;
  text-rendering: optimizeLegibility;
  color: #444;
  background: #eee;
  color: #dd5;
}

h1 {
  font-weight: normal;
  letter-spacing: -1px;
  color: #34495e;
}

.rwd-table {
  background: #34495e;
  color: #fff;
  border-radius: 0.4em;
  overflow: hidden;
}

#sector3 {
  margin: 0 auto;
  display: flex;
}
</style>
