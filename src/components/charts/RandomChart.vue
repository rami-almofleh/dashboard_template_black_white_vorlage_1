<template>
  <div class="chart-container">
    <canvas id="barChart"></canvas>
  </div>
</template>
<script>
import { Chart, registerables } from "chart.js";

export default {
  data () {
    return {
      chart: null,
      type: 'bar',
      data: {
        labels: ['JAN', 'FEB', 'MAR', 'APR', 'MAY', 'JUN', 'JUL', 'AUG', 'SEP', 'OCT', 'NOV', 'DES'],
        datasets: [{
          label: '',
          data: [2000, 2500, 7500, 5000, 1000, 2000, 5000, 2000, 2500, 6000, 2000, 1000],
          backgroundColor: '#333'
        }]
      },
      options: {
        scales: {
          y: {
            beginAtZero: true
          },
          xAxes: {
            gridLines: {
              display: false
            }
          }
        }
      }
    }
  },
  mounted() {
    // chart.js 3 is ESM tree shakeable and requires to register all components that you are going to use. Thus, you have to register the linear scale manually
    // https://www.chartjs.org/docs/next/getting-started/integration.html
    Chart.register(...registerables);

    const ctx = document.getElementById('barChart').getContext('2d');
    this.chart = new Chart(ctx, {type: this.type, data: this.data, options: this.options})
  }
}
</script>

<style lang="scss" scoped>
.chart-container {
  width: 100%;
  position: relative;
  canvas {
    height: 22rem !important;
  }
}
</style>
