<template>
  <div class="card shadow-lg border-0 rounded-standard bg-dark text-white" style="width: 21rem">
    <div class="card-body">
      <h5 class="card-title mb-3">
        <i class="bi bi-sim fs-1 text-white-50 mb-3 d-block"></i>
        <h4>4353 4445 5690 7634</h4>
      </h5>
      <div class="card-text d-flex justify-content-between align-items-end">
        <p class="text-muted">-------</p>
        <i class="bi bi-card-image fs-3"></i>
      </div>
      <div class="card-text d-flex justify-content-between align-items-start">
        <p>-----------</p>
        <p>Mastercard</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CreditCard"
}
</script>

<style scoped lang="scss">
.card {
  background-image: linear-gradient(to left top, #000000, #545555);
}
</style>
