<template>
  <div class="c-navbar px-3 px-lg-5 pt-3 pt-lg-4 row">
    <div class="col-auto">
      <h2 class="mb-0 pt-2" style="font-weight: 900">Dashboard</h2>
      <p class="fw-light mb-4">Payments updates</p>
    </div>
    <div class="col d-flex align-items-center" style="width: 20rem">
      <div class="input-group rounded-pill bg-white mx-auto d-none d-lg-flex">
        <span class="input-group-text bg-transparent border-0" id="basic-addon1">
          <i class="bi bi-search"></i>
        </span>
        <input type="search" class="form-control input-outline-none bg-transparent border-0 ps-0" placeholder="Search" aria-label="Search" aria-describedby="basic-addon1">
      </div>
    </div>
    <div class="col-auto d-flex align-items-center">
      <div class="dropdown d-inline-block">
        <a class="nav-link dropdown-toggle pe-2" href="#" id="navbarScrollingDropdownBell" role="button" data-bs-toggle="dropdown" aria-expanded="false">
          <i class="bi bi-bell fs-4"></i>
        </a>
        <ul class="dropdown-menu notifications dropdown-bottom-right p-0" aria-labelledby="navbarScrollingDropdownBell">
          <li class="notification-item"><a class="dropdown-item" href="#">
            <div class="notification py-2">
              <h6 class="mb-1 fw-bold">Paul</h6>
              <p class="mb-0">This is a wider card with supporting text below as a...</p>
            </div>
          </a></li>
          <li class="notification-item"><a class="dropdown-item" href="#">
            <div class="notification py-2">
              <h6 class="mb-1 fw-bold">Rene</h6>
              <p class="mb-0">This is a wider card with supporting text below as a...</p>
            </div>
          </a></li>
          <li class="notification-item"><a class="dropdown-item" href="#">
            <div class="notification py-2">
              <h6 class="mb-1 fw-bold">Katja</h6>
              <p class="mb-0">This is a wider card with supporting text below as a...</p>
            </div>
          </a></li>
        </ul>
      </div>

      <div class="d-inline-block dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarScrollingDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
          <i class="bi bi-person-circle fs-4"></i>
        </a>
        <ul class="dropdown-menu dropdown-bottom-right" aria-labelledby="navbarScrollingDropdown">
          <li><a class="dropdown-item border-bottom" href="#">My profile</a></li>
          <li><a class="dropdown-item" href="#">Settings</a></li>
          <li><hr class="dropdown-divider"></li>
          <li><a class="dropdown-item" href="#">Logout</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar"
}
</script>

<style lang="scss" scoped>
.dropdown-bottom-right.dropdown-menu[data-bs-popper] {
  left: unset !important;
  right: 0 !important;
}
#navbarScrollingDropdownBell {
  &.dropdown-toggle {
    &:after {
      display: none;
    }
  }
}

.input-group.rounded-pill {
  max-width: 16rem;
  border: 1px solid #eeeeee
}
.notification-item {
  border-bottom: 1px solid #cccccc;
  p {
    white-space: break-spaces;
    width: 16rem;
    line-height: 1.1rem;
  }
}
.notifications {
  .notification:last-child {
    .notification-item {
      border-bottom: none;
    }
  }
}
</style>
