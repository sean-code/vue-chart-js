<template>

<div class="chart-container">

  <Pie
    id="my-chart-id"
    :options="chartOptions"
    :data="chartData"
    :style="{ width: '80%', margin: '0 auto' }"
  />

</div>
</template>

<script>
import { Pie } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, ArcElement } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, ArcElement)

export default {
  name: 'PieChart',
  components: { Pie },
  data() {
    return {
      chartData: {
        labels: [ 'January', 'February', 'March', "April", "May", "June", "July" ],
        datasets: [ {
          data: [40, 20, 120, 150, 100, 400, 350],
          backgroundColor: [
          'rgba(255, 99, 132, 0.8)', // Red
            'rgba(54, 162, 235, 0.8)', // Blue
            'rgba(255, 206, 86, 0.8)', // Yellow
            'rgba(75, 192, 192, 0.8)', // Green
            'rgba(153, 102, 255, 0.8)', // Purple
            'rgba(255, 159, 64, 0.8)', // Orange
            'rgba(94, 94, 94, 0.8)'
          ]
        } ]
      },
      chartOptions: {
        responsive: true,
        cutoutPercentage: 60
      }
    }
  }
}
</script>


<style scoped>
.chart-container {
  text-align: center;
}
</style>
