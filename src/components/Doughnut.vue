<template>
     <div class="chart-container">
         <Doughnut
           id="my-chart-id"
           :options="chartOptions"
           :data="chartData"
         />
     </div>
  </template>

  <script>
  import { Doughnut } from 'vue-chartjs'
  import { Chart as ChartJS, Title, Tooltip, Legend, ArcElement } from 'chart.js'

  ChartJS.register(Title, Tooltip, Legend, ArcElement)

  export default {
    name: 'DoughnutChart',
    components: { Doughnut },
    data() {
      return {
        chartData: {
          labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
          datasets: [
            {
              data: [40, 20, 120, 150, 100, 400, 350],
              backgroundColor: [
                '#FF6384',
                '#36A2EB',
                '#FFCE56',
                '#4BC0C0',
                '#9966FF',
                '#FF9F40',
                '#F7464A'
              ],
              borderWidth: 1
            }
          ]
        },
        chartOptions: {
          responsive: true,
          cutoutPercentage: 40
        }
      }
    }
  }
  </script>


<style scoped>


.chart-container {
  display: flex;
  justify-content: center;
  align-items: center;
  /* Add additional styling as needed */
}
</style>
