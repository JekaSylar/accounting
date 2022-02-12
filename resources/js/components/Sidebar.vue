<template>
  <ul class="sidenav app-sidenav" :class="status">
    <li v-for="link in links" :key="link.url">
      <router-link :to="link.url" class="waves-orange pointer">{{
        link.title
      }}</router-link>
    </li>
  </ul>
</template>

<script>
export default {
  props: ["status"],

  data() {
    return {
      links: [
        { title: "Счет", url: "/" },
        { title: "История", url: "/history" },
        { title: "Планирование", url: "/planning" },
        { title: "Новая запись", url: "/record" },
        { title: "Категории", url: "/categories" },
      ],
    };
  },
};
</script>

<style scoped>
.router-link-active {
  background-color: #ffa726 !important;
}
</style>
