<template>
  <ChartVue />

  <!-- Uupdate Charts -->
    <div>
      <h1>My Pie Chart</h1>
    <PieChart />
    </div>


    <h1>Bubble Chart</h1>
    <BubbleChart />
</template>

<script setup>
import ChartVue from "./components/ChartVue.vue";
import PieChart from './components/PieChart.vue';
import BubbleChart from "./components/Bubble.vue";


</script>

<style>

</style>
