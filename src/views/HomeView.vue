<template>
  <div class="px-3 px-lg-5 px-lg-4 row pro-page">
    <div>
      <payments-updates />
      <balance />
      <transection-history />
    </div>
    <div class="col-lg-5 col-xl-4 pt-5 pt-lg-4 px-3 px-lg-5">
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
$page_right_width : 25rem;

.pro-page {
  > div:nth-child(1) {
    width: 100%;
    @media (min-width: 1200px) {
      width: calc(100% - $page_right_width);
    }
  }
  > div:nth-child(2) {
    width: 100%;
    @media (min-width: 1200px) {
      width: $page_right_width;
    }
  }
}
</style>
