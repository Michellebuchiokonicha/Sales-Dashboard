<script setup>
import { RouterView } from "vue-router";
import Sidebar from "./components/SideBar.vue";
</script>

<template>
    <div class="app">
      <Sidebar/>

      <RouterView />

      
    </div>
 

  
</template>

<style lang="scss">
:root {
  --primary: teal;
  --primary-alt: rgb(31, 90, 90);
  --grey: rgb(104, 184, 184);
  --dark: rgb(25, 160, 160);
  --dark-alt: rgb(108, 206, 206);
  --light: #f1f5f9;
  --sidebar-width: 300px;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
body {
  background: var(--light);
}

button {
  cursor: pointer;
  appearance: none;
  border: none;
  outline: none;
  background: none;
}
.app {
  display: flex;

  main {
    flex: 1 1 0;
    padding: 2rem;

    @media (max-width: 760px) {
      padding-left: 6rem;
    }
  }
}

@media (hover: hover) {
 

@media (min-width: 1024px) {
 
}
}
</style>


