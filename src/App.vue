<template>
  <h1 style="text-align: center;">Vue Chart JS</h1>
  <div class="parent">
    <div class="chart-container">
    <div class="chart-box">
      <h2>Bar Chart</h2>
      <ChartVue />
    </div>

    <div class="chart-box">
      <h2>Pie Chart</h2>
      <p>They are excellent at showing the relational proportions between data.</p>
      <PieChart />
    </div>

    <div class="chart-box">
      <h2>Doughnut Chart</h2>
      <p>They are excellent at showing the relational proportions between data.</p>
      <Doughnut />
    </div>

    <div class="chart-box">
      <h2>Bubble Chart</h2>
      <BubbleChart />
    </div>

    <!-- Radar Chart - uncomment if needed -->
    <!-- <div class="chart-box">
      <h2>Radar Chart</h2>
      <p>
        A radar chart is a way of showing multiple data points and the variation between them.
        <br>They are often useful for comparing the points of two or more different data sets.
      </p>
    </div> -->
  </div>
  </div>
  <div class="footer">
    Created by Sean Code<br>© 2023
  </div>
</template>

<script setup>
import ChartVue from "./components/ChartVue.vue";
import PieChart from './components/PieChart.vue';
import BubbleChart from "./components/Bubble.vue";
import Doughnut from "./components/Doughnut.vue"
</script>

<style scoped>

.parent{
  /* background-color: rgba(126, 158, 158, 0.076); */
  background: rgba(0, 0, 0, 0.2) url('https://img.freepik.com/free-photo/white-painted-wall-texture-background_53876-138197.jpg?size=626&ext=jpg');
  background-blend-mode: darken;
  background-repeat: none;
}
.chart-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 50px;
}

.chart-box {
  border: 1px solid #60ff04;
  border-radius: 8px;
  padding: 16px;
  margin: 16px;
  max-width: 300px;
  text-align: center;
  background-color: rgba(227, 237, 237, 0.739);
}
</style>
