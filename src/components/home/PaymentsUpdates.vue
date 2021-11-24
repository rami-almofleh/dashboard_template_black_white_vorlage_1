<template>
  <p class="fw-light">Payments updates</p>
  <div class="gap-4 mt-4 d-flex flex-wrap flex-lg-nowrap">
    <div v-for="payment in payments" :key="payment" class="flex-grow-1 d-flex align-content-stretch w-25">
      <payments-updates-item :payment="payment" />
    </div>
  </div>
</template>

<script>
import PaymentsUpdatesItem from "./PaymentsUpdatesItem";
export default {
  name: "PaymentsUpdates",
  components: {PaymentsUpdatesItem},
  data () {
    return {
      payments: [
        {
          title: '$1200',
          subtitle: 'Transfer via Card number',
          img: 'bi bi-credit-card',
        },
        {
          title: '$150',
          subtitle: 'Transfer other Banks',
          img: 'bi-arrow-left-right',
        },
        {
          title: '$1760',
          subtitle: 'Transfer some Bank',
          img: 'bi bi-bank',
        },
        {
          title: '$1400',
          subtitle: 'Transfer to other Bank',
          img: 'bi bi-cash-coin',
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
