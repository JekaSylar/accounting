<template>
  <div class="app-main-layout">
    <navbar @clickHiden="isOpen = !isOpen" />
    <sidebar :status="isOpen ? 'hiden' : 'open'" />
    <main class="app-content" :class="{ full: isOpen }">
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
  data() {
    return {
      isOpen: false,
    };
  },

  components: {
    Navbar,
    Sidebar,
    AddRecord,
  },
};
</script>

<style>
</style>
