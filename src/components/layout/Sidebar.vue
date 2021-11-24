<template>
  <div class="d-none d-lg-flex flex-column flex-shrink-0 bg-transparent h-100 position-fixed start-0 bottom-0" style="width: 4.5rem;">
    <a href="/" class="d-block p-3 link-dark text-decoration-none" title="Icon-only" data-bs-toggle="tooltip" data-bs-placement="right">
      <i class="bi bi-image-fill fs-1"></i>
      <span class="visually-hidden">Icon-only</span>
    </a>
    <ul class="nav nav-pills nav-flush flex-column mb-auto text-center fs-3">
      <li class="nav-item">
        <a href="#" class="nav-link p-2 rounded-0" :class="{'active' : selected_tab === 'home'}" @click="selected_tab = 'home'" aria-current="page" title="Home" data-bs-toggle="tooltip" data-bs-placement="right">
          <i class="bi bi-house"></i>
        </a>
      </li>
      <li>
        <a href="#" class="nav-link p-2 rounded-0" :class="{'active' : selected_tab === 'orders'}" @click="selected_tab = 'orders'" title="Orders" data-bs-toggle="tooltip" data-bs-placement="right">
          <i class="bi bi-archive"></i>
        </a>
      </li>
      <li>
        <a href="#" class="nav-link p-2 rounded-0" :class="{'active' : selected_tab === 'products'}" @click="selected_tab = 'products'" title="Products" data-bs-toggle="tooltip" data-bs-placement="right">
          <i class="bi bi-grid"></i>
        </a>
      </li>
      <li>
        <a href="#" class="nav-link p-2 rounded-0" :class="{'active' : selected_tab === 'customers'}" @click="selected_tab = 'customers'" title="Customers" data-bs-toggle="tooltip" data-bs-placement="right">
          <i class="bi bi-people"></i>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      selected_tab: 'home'
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/styles/global.scss";

.nav-link {
  color: rgba(0,0,0,.3);

  &.active {
     background: transparent !important;
     color: $primary !important;
     border-right: 3px solid $primary !important;
   }
}
</style>
