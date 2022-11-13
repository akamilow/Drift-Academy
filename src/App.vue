<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header class="header-home">
    <nav class="main-menu">
        <div>
            <img
              id="header-img"
              src="@/assets/img/evisu.png"             
            />
        </div>
        <ul class="menu-link-desktop">
            <RouterLink class="nav-link" to="/">Home</RouterLink>
            <RouterLink class="nav-link" to="/cars">Cars</RouterLink>
            <RouterLink class="nav-link" to="/circuits">Circuits</RouterLink>
            <RouterLink class="nav-link cta-btn" to="/join">JOIN</RouterLink>  
        </ul>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
</style>