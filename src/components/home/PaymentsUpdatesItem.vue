<template>
  <div class="card shadow-lg border-0 rounded-standard w-100">
    <div class="card-body px-4">
      <i class="fw-bolder" :class="payment.img" style="font-size: 2.5rem;"></i>
      <h6 class="card-text text-black-50 pt-3">{{ payment.subtitle }}</h6>
      <h3 class="card-title fw-bolder text-capitalize mb-0">{{ payment.title }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "PaymentsUpdatesItem",
  props: ['payment']
}
</script>

<style lang="scss" scoped>
</style>
