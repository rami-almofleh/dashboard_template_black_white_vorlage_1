<template>
  <h2 class="mt-5 mb-0" style="font-weight: 900">Recent activities</h2>
  <p class="fw-light mb-4">02 Mars 2021</p>
  <div class="row mb-2" v-for="item in recent_activities" :key="item">
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
      recent_activities: [
        {
          icon: 'bi bi-droplet-half',
          title: 'Water Bill',
          subtitle: 'Successfully',
          price: '$120'
        },
        {
          icon: 'bi bi-cash-stack',
          title: 'Income Salary',
          subtitle: 'Received',
          price: '$4500'
        },
        {
          icon: 'bi bi-lightning',
          title: 'Electric Bill',
          subtitle: 'Successfully',
          price: '$70'
        },
        {
          icon: 'bi bi-wifi',
          title: 'Internet Bill',
          subtitle: 'Successfully',
          price: '$55'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
