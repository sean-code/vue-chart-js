<template>
  <ChartVue />

  <!-- Uupdate Charts -->
    <div>
      <h1>My Pie Chart</h1>
      <p>They are excellent at showing the relational proportions between data.</p>
    <PieChart />
    </div>


    <h1>Bubble Chart</h1>
    <BubbleChart />


    <h1>Doughnut Chart</h1>
    <p>They are excellent at showing the relational proportions between data.</p>
    <Doughnut />

    <h1>Radar Chart</h1>
    <p>
      A radar chart is a way of showing multiple data points and the variation between them.
      <br>They are often useful for comparing the points of two or more different data sets.
    </p>
</template>

<script setup>
import ChartVue from "./components/ChartVue.vue";
import PieChart from './components/PieChart.vue';
import BubbleChart from "./components/Bubble.vue";
import Doughnut from "./components/Doughnut.vue"


</script>

<style>

</style>
