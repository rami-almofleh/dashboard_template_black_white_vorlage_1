<template>
  <h2 class="mt-5 mb-0 text-nowrap" style="font-weight: 900">Upcoming Payments</h2>
  <p class="fw-light mb-4">11 Mars 2021</p>

  <div class="row mb-2" v-for="item in upcoming_payments" :key="item">
    <div class="col-auto">
      <div class="bg-white rounded-pill d-flex align-items-center justify-content-center" style="height: 3rem; width: 3rem">
        <i class="fs-4" :class="item.icon"></i>
      </div>
    </div>
    <div class="col-6">
      <p class="m-0" style="font-weight: 900">{{ item.title }}</p>
      <p class="m-0 text-light text-black-50 small">{{ item.subtitle }}</p>
    </div>
    <div class="col-auto" style="font-weight: 900">{{ item.price }}</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      upcoming_payments: [
        {
          icon: 'bi bi-house',
          title: 'House Rent',
          subtitle: 'Pending',
          price: '$1200'
        },
        {
          icon: 'bi bi-truck',
          title: 'Car Rent',
          subtitle: 'Successfully',
          price: '$150'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
