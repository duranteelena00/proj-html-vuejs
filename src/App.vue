<template>
  <div id="app">
    <Header :contacts="contacts" :links="links" />
    <Content :contacts="contacts" />
    <Footer :contacts="contacts" :links="links" />
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

body {
  width: 100vw;
  height: 100%;
  overflow-x: hidden;
  overflow-y: scroll;
}

#app {
  width: 100vw;
  height: 100%;
  overflow-x: hidden;
  overflow-y: scroll;
  font-family: "Montserrat", sans-serif;
}

section {
  padding: 70px 0;
  width: 100%;
}

h1 {
  font-weight: 900;
}

h2 {
  font-size: 30px;
  font-weight: 800;
  span.turquoise {
    color: #038483;
    background: rgb(218, 236, 237);
    border-radius: 5px;
  }
}

.text > h4 {
  color: #038483;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  color: currentColor;
}

p {
  font-size: 14px;
  line-height: 22px;
}

.logo-container {
  height: 65px;
  line-height: 65px;
  .logo {
    font-family: Arial;
    font-size: 16px;
    font-weight: bold;
    span:nth-of-type(2) {
      margin-left: 3px;
      color: white;
    }
    span.turquoise {
      padding: 10px 4px 10px 25px;
      background: rgba(60, 175, 175, 0.2);
      color: #038483;
      border-radius: 30px 0 0 30px;
    }
  }
}

.card {
  min-height: 100%;
  padding: 25px 20px 40px 30px;
  border-radius: 5px;
  &:hover {
    transform: scale(1.1);
  }
  i {
    margin: 0;
    color: teal;
  }
}

.dots {
  height: 40px;
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1;
}

input {
  padding: 10px 20px;
  border: none;
}

button.turquoise {
  padding: 10px 20px;
  color: white;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  background: #038483;
}

button.transparent {
  padding: 10px 20px;
  color: white;
  font-weight: bold;
  border: 1px solid #038483;
  border-radius: 5px;
  background: transparent;
}

/* Utils */
.container {
  display: flex;
}

.light-turquoise {
  background: rgb(238, 244, 237);
}

.dark-darkblue {
  color: rgb(192, 195, 208);
  background: rgb(17, 17, 23);
}
</style>
