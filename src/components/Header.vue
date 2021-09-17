<template>
  <header>
    <div id="find-the-company">
      <div class="container">
        <span><i class="fas fa-clock me-2"></i>{{ contacts.openHours }}</span>
        <ul class="d-flex align">
          <li class="ms-4">
            <i class="fas fa-phone-alt me-2"></i>{{ contacts.number }}
          </li>
          <li class="ms-4">
            <i class="fas fa-envelope me-2"></i>{{ contacts.email }}
          </li>
          <li class="ms-4"><i class="fab fa-facebook-f"></i></li>
          <li class="ms-4"><i class="fab fa-twitter"></i></li>
          <li class="ms-4"><i class="fab fa-linkedin-in"></i></li>
        </ul>
      </div>
    </div>
    <section class="jumbotron" id="hero">
      <img class="background" src="@/assets/img/hero-image.png" alt="" />
      <nav id="main-menu">
        <div class="container">
          <div class="logo-container">
            <span class="logo"
              ><span class="turquoise">NEX</span><span>GEN</span></span
            >
          </div>
          <ul class="d-flex">
            <li class="ms-4" v-for="link in links" :key="link.id">
              <a class="link" href="#">{{ link.toUpperCase() }}</a>
            </li>
            <li><button class="ms-4 turquoise">GET IN TOUCH</button></li>
          </ul>
        </div>
      </nav>
      <div class="jumbotron-text">
        <h1>Lead ~ Customer</h1>
        <p class="my-3 text-center">
          Successful strategies require data analysis, creativity and customer
          focus, taking advantage of the latest technologies to offer excellent
          services.
        </p>
        <button class="mx-1 turquoise" type="button">GET IN TOUCH</button>
        <button class="mx-1 transparent" type="button">READ MORE</button>
      </div>
    </section>
    <section id="company-benefits" class="light-turquoise">
      <div class="container">
        <div class="row">
          <div class="col-4">
            <div class="card">
              <i class="fas fa-users"></i>
              <h3 class="my-3">Human Capital</h3>
              <p>
                Humanizing business: Harness the power of technology to improve
                the way people work.
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <i class="fas fa-chart-pie"></i>
              <h3 class="my-3">Core Business</h3>
              <p>
                It takes innovative approaches to transform, modernize and run
                existing platform.
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <i class="fas fa-chart-line"></i>
              <h3 class="my-3">Performance</h3>
              <p>
                Acheaving maximum impact and value from investments in finance
                and supply chains.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    contacts: Object,
    links: Array,
  },
};
</script>

<style lang="scss" scoped>
header {
  #find-the-company {
    color: rgb(187, 187, 187);
    height: 40px;
    background: rgb(45, 64, 77);
    display: flex;
    align-items: center;
    font-size: 12px;
    .container {
      justify-content: space-between;
    }
  }
}

header > .jumbotron {
  background: black;
  height: 500px;
  position: relative;
  img.background {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    opacity: 0.3;
  }
  .jumbotron-text {
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 14px;
    h1 {
      color: white;
      font-size: 45px;
    }
    p {
      color: rgb(149, 149, 149);
    }
  }
}

#main-menu {
  height: 65px;
  width: 100%;
  z-index: 2;
  background-color: transparent;
  font-size: 12px;
  position: absolute;
  top: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  .container {
    display: flex;
    .logo-container {
      flex-grow: 1;
    }
    ul {
      width: fit-content;
      align-items: center;
      li > a {
        color: white;
      }
    }
  }
}

header > #company-benefits {
  display: flex;
  align-items: center;
  .container {
    display: flex;
    align-items: center;
    .row {
      height: fit-content;
    }
  }
}

.card {
  background: white;
  i {
    margin: 0;
    padding: 12.5px;
    color: teal;
    font-size: 25px;
    border-radius: 50%;
    background: rgb(218, 236, 237);
  }
  h3 {
    font-weight: 700;
  }
  p {
    color: rgb(148, 147, 147);
  }
}
</style>