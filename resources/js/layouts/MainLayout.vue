<template>
  <div class="app-main-layout">
    <navbar />
    <sidebar />
    <main class="app-content">
      <div class="app-page">
        <router-view />
      </div>
    </main>
    <add-record />
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Sidebar from "../components/Sidebar.vue";
import AddRecord from "../components/AddRecord.vue";
export default {
  components: {
    Navbar,
    Sidebar,
    AddRecord,
  },
};
</script>

<style>
</style>
