<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid px-lg-4 d-flex justify-content-between flex-nowrap align-items-end">
      <h2 class="m-0" style="font-weight: 900">Dashboard</h2>

      <div class="input-group rounded-pill bg-white">
        <span class="input-group-text bg-transparent border-0" id="basic-addon1">
          <i class="bi bi-search"></i>
        </span>
        <input type="search" class="form-control input-outline-none bg-transparent border-0 ps-0" placeholder="Search" aria-label="Search" aria-describedby="basic-addon1">
      </div>

      <div class="d-flex align-items-center gap-1">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScrollBell" aria-controls="navbarScrollBell" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarScrollBell">
          <ul class="navbar-nav me-auto p-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarScrollingDropdownBell" role="button" data-bs-toggle="dropdown" aria-expanded="false">
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
            </li>
          </ul>
        </div>


        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarScroll">
          <ul class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarScrollingDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                <i class="bi bi-person-circle fs-4"></i>
              </a>
              <ul class="dropdown-menu dropdown-bottom-right" aria-labelledby="navbarScrollingDropdown">
                <li><a class="dropdown-item" href="#">My profile</a></li>
                <li><a class="dropdown-item" href="#">Settings</a></li>
                <li><hr class="dropdown-divider"></li>
                <li><a class="dropdown-item" href="#">Logout</a></li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
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
#navbarScrollBell {
  .dropdown-toggle {
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
