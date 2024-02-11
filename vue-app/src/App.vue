<script setup>
import SideBar from './components/SideBar.vue';
</script>

<template>
  <v-app>
    <SideBar />
    <v-main>
        Test
    </v-main>
  </v-app>
</template>

<style lang="scss">
  :root {
    --primary: #4ade80;
    --grey: #64748b;
    --dark: #1e293b;
    --dark-alt: #334155;
    --light: #f1f5f9;
  } 

  v-main{
    height: 280px;
  }
</style>