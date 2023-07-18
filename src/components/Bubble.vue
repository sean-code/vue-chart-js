<template>
    <Bubble
      id="my-chart-id"
      :options="chartOptions"
      :data="chartData"
    />
  </template>

  <script>
  import { Bubble } from 'vue-chartjs'
  import { Chart as ChartJS, Title, Tooltip, Legend, PointElement } from 'chart.js'

  ChartJS.register(Title, Tooltip, Legend, PointElement)

  export default {
    name: 'BubbleChart',
    components: { Bubble },
    data() {
      return {
        chartData: {
          datasets: [
            {
              label: 'Data Points',
              data: [
                { x: 'January', y: 40, r: 10 },
                { x: 'February', y: 20, r: 5 },
                { x: 'March', y: 12, r: 3 },
                { x: 'April', y: 50, r: 15 },
                { x: 'May', y: 100, r: 20 },
                { x: 'June', y: 400, r: 40 },
                { x: 'July', y: 350, r: 35 }
              ],
              backgroundColor: 'rgba(54, 162, 235, 0.6)',
              hoverBackgroundColor: 'rgba(54, 162, 235, 1)'
            }
          ]
        },
        chartOptions: {
          responsive: true
        }
      }
    }
  }
  </script>
