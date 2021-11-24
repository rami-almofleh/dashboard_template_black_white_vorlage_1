<template>
  <h2 class="mt-5 mb-0" style="font-weight: 900">Balance</h2>
  <div class="d-flex justify-content-between align-items-end mb-4">
    <p class="fw-bolder mb-4">$1500</p>
    <p class="text-muted">Past 30 days</p>
  </div>
  <random-chart />
</template>

<script>
import RandomChart from "../charts/RandomChart";
export default {
  name: "Balance",
  components: {RandomChart}
}
</script>
