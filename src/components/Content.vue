<template>
  <section class="content">
    <Main />
    <section id="business-news">
      <div class="container"></div>
    </section>
    <section id="newsletter"></section>
    <section id="contact-us">
      <div class="container">
        <div class="form"></div>
        <div id="contacts"></div>
      </div>
    </section>
  </section>
</template>

<script>
import Main from "./components/Main.vue";

export default {
  name: "Content",
  components: Main
};
</script>

<style lang="scss" scoped>
</style>