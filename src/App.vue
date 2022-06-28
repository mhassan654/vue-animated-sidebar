/* eslint-disable */
<template>
  <div>
    <!-- <Navbar /> -->
    <div class="app">
      <Sidebar />

      <router-view />
      <!-- <router-link to="/">Home</router-link> | -->
      <!-- <router-link to="/about">About</router-link> -->
    </div>
  </div>

  <!--  -->
</template>
<script setup>
import Sidebar from "./components/SideBar.vue";
// eslint-disable-next-line
// import Navbar from "./components/NavBar.vue";
</script>

<style lang="scss">
:root{
  --primary: #1A8DD2;
  --primary-alt: #22c55e
  --grey: #64748b;
  --dark: #1e293b;
  --dark-alt:#334155;
  --light: #f1f5f9;
  --sidebar-width: 240px;
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Fira sans',sans-serif;
}

body{
  background: var(--light);
}
button{
  cursor: pointer;
  appearance:none;
  border: none;
  outline: none;
  background: none;
}
.app{
  display: flex;
  main{
    flex: 1 1 0;
    padding: 2rem;

    @media(max-width: 768px) {
      padding-left: 6rem;
    }
  }
}
main{
  background: #F8FAFB;
}
</style>
