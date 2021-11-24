<template>
  <h2 class="mt-5 mb-0" style="font-weight: 900">History</h2>
  <p class="fw-light mb-4">Transaction of last 6 months</p>

  <div class="w-100 table-container">
    <div :class="{'bg-white rounded-pill shadow-lg' : item.id === 1}" class="row py-3 d-flex align-items-center w-100" style="width: max-content" v-for="item in transection_history" :key="item.title">
      <div class="col-auto">
        <div class="avatar rounded-circle overflow-hidden">
          <img :src="item.image" alt="" />
        </div>
      </div>
      <div class="col-4">{{ item.title }}</div>
      <div class="col-2">{{ item.time }}</div>
      <div class="col-2">{{ item.price }}</div>
      <div class="col-2">{{ item.status }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      transection_history: [
        {
          id: 1,
          image: 'https://cdn.pixabay.com/photo/2020/12/30/14/23/waterfall-5873630_1280.jpg',
          title: 'Car Insurance',
          time: '11:23 AM',
          price: '$1150.0',
          status: 'Completed'
        },
        {
          id: 2,
          image: 'https://media.istockphoto.com/photos/fossli-provin…k-vancouver-island-picture-id1285518457?s=612x612',
          title: 'Jacob',
          time: '10:15 AM',
          price: '$210.0',
          status: 'Completed'
        },
        {
          id: 3,
          image: 'https://media.istockphoto.com/photos/sunset-hike-to-sweet-creek-falls-in-oregon-picture-id1156838527?s=612x612',
          title: 'Laon',
          time: '02:10 PM',
          price: '$143.0',
          status: 'Completed'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.avatar {
  height: 3rem;
  width: 3rem;
}
.table-container {
  word-wrap: break-word;
  hyphens: auto;
  @media (max-width: 990px) {
    overflow-x: auto;
  }
}
</style>
