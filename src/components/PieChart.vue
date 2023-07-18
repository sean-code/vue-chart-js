<template>
  <Pie
    id="my-chart-id"
    :options="chartOptions"
    :data="chartData"
  />
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
        datasets: [ { data: [40, 20, 120, 150, 100, 400, 350] } ]
      },
      chartOptions: {
        responsive: true,
        cutoutPercentage: 60
      }
    }
  }
}
</script>
