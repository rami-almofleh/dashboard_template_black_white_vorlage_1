<template>
  <div class="row px-5">
    <div class="col-xl-9 pt-3">
      <payments-updates />
      <balance />
      <transection-history />
    </div>
    <div class="col-xl-3 pt-3">
      <credit-card />
      <recent-activities />
      <upcoming-payments />
    </div>
  </div>
</template>

<script>
import PaymentsUpdates from "../components/home/PaymentsUpdates";
import CreditCard from "../components/home/CreditCard";
import Balance from "../components/home/Balance";
import TransectionHistory from "../components/home/TransectionHistory";
import RecentActivities from "../components/home/RecentActivities";
import UpcomingPayments from "../components/home/UpcomingPayments";
export default {
  name: "HomeView",
  components: {UpcomingPayments, RecentActivities, TransectionHistory, Balance, CreditCard, PaymentsUpdates}
}
</script>

<style lang="scss" scoped>

</style>
