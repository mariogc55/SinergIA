<template>
  <div class="app-layout">
    <SidebarNav />
    <div class="main-content">
      <header class="top-bar">
        <JiraProjectSelector />
      </header>
      <main class="page-content">
        <router-view /> 
      </main>
    </div>
  </div>
</template>

<script setup>
import SidebarNav from './SidebarNav.vue';
import JiraProjectSelector from './JiraProjectSelector.vue';
// No se necesita mucha lógica aquí, solo la estructura.
</script>

<style scoped>
.app-layout {
    display: flex;
    height: 100vh;
}

.main-content {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    overflow-y: hidden;
}

.top-bar {
    height: 60px;
    padding: 0 20px;
    background-color: white;
    border-bottom: 1px solid #ddd;
    display: flex;
    align-items: center;
    justify-content: flex-end; /* Alinea el selector a la derecha */
}

.page-content {
    flex-grow: 1;
    padding: 20px;
    overflow-y: auto; /* Permite desplazamiento en el contenido de la página */
    background-color: #f4f4f9;
}
</style>