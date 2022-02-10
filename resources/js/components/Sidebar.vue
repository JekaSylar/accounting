<template>
  <ul class="sidenav app-sidenav open">
    <li v-for="link in links" :key="link.url">
      <router-link :to="link.url" class="waves-effect waves-orange pointer">{{
        link.title
      }}</router-link>
    </li>
  </ul>
</template>

<script>
export default {
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

<style>
</style>
