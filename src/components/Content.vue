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
  components: Main,
  data(){
    return {
     news: [
       {imgUrl: "src/assets/img/news-1.jpg",
       title: "Increasing creativity is possible for everyone"},
       {imgUrl: "src/assets/img/news-2.jpg",
       title: "Becouse market research is part of the business plan"},
       {imgUrl: "src/assets/img/news-3.jpg",
       title: "Work from home is now a trend"},
     ]
    }
  }
};
</script>

<style lang="scss" scoped>
</style>