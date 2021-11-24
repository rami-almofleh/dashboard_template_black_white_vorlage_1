<template>
  <main>
    <sidebar class="d-inline-block" />
    <div class="pro-body position-fixed top-0 bottom-0 end-0 d-inline-block">
      <Navbar />
      <router-view />
    </div>
  </main>
</template>

<script>

import Sidebar from "./components/layout/Sidebar";
import Navbar from "./components/layout/Navbar";
export default {
  name: 'App',
  components: {Navbar, Sidebar}
}
</script>

<style lang="scss" scoped>

  main {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    height: 100vh;
    max-height: 100vh;
  }
  .pro-body {
    width: calc(100% - 4.5rem);
    overflow-y: auto;
    overflow-x: hidden;
    @media (max-width: 990px) {
      width: 100%;
    }
  }
</style>
