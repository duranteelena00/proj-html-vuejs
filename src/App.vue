<template>
  <div id="app">
    <Header />
    <Content />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer,
  },
  data() {
    return {
      logoUrl: "src/assets/img/logo_48.png",
      contacts: {
        "Open Hours": "Mon-Sat - 9:00-18:00",
        number: "+1(305)1234-5678",
        email: "hello@example.com",
        office: "Main Avenue, 987",
        links: ["Home", "About", "Services", "Pricing", "Blog"]
      },
    };
  },
};
</script>

<style lang="scss">
/* Generals */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  width: 100vw;
  height: 100%;
  overflow-x: hidden;
  font-family: sans-serif, Arial, Helvetica;
}
</style>
