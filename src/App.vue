<template>
  <div id="app">
    <Header :contacts="contacts" :links="links" />
    <Content />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Content from "@/components/Content.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer,
  },
  data() {
    return {
      contacts: {
        openHours: "Mon-Sat - 9:00-18:00",
        number: "+1(305)1234-5678",
        email: "hello@example.com",
        office: "Main Avenue, 987",
      },
      links: ["Home", "About", "Services", "Pricing", "Blog"],
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
  overflow-y: scroll;
  font-family: Helvetica;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: currentColor;
}

p {
  line-height: 23px;
}

/* Utils */
.container {
  display: flex;
}

button.turquoise {
  padding: 10px 20px;
  color: white;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  background: rgb(1, 170, 170);
}

button.transparent {
  padding: 10px 20px;
  color: white;
  font-weight: bold;
  border: 1px solid rgb(1, 170, 170);
  border-radius: 5px;
  background: transparent;
}
</style>
