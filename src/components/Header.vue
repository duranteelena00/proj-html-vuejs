<template>
  <header>
    <div id="find-the-company">
      <div class="container">
        <span>{{ contacts.openHours }}</span>
        <ul class="d-flex align">
          <li class="ms-4">
            <i class="fas fa-phone-alt me-1"></i>{{ contacts.number }}
          </li>
          <li class="ms-4">
            <i class="fas fa-envelope me-1"></i>{{ contacts.email }}
          </li>
          <li class="ms-4"><i class="fab fa-facebook-f"></i></li>
          <li class="ms-4"><i class="fab fa-twitter"></i></li>
          <li class="ms-4"><i class="fab fa-linkedin-in"></i></li>
        </ul>
      </div>
    </div>
    <section class="jumbotron" id="hero">
      <img src="@/assets/img/hero-image.png" alt="" />
      <nav id="main-menu">
        <div class="container m-0 p-0">
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
    <section id="company-benefits">
      <div class="container">
        <div class="row">
          <div class="col-4">
            <div class="card">
              <i class="fas fa-users"></i>
              <h4 class="my-3">Human Capital</h4>
              <p>
                Humanizing business: Harness the power of technology to improve
                the way people work.
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <i class="fas fa-chart-pie"></i>
              <h4 class="my-3">Core Business</h4>
              <p>
                It takes innovative approaches to transform, modernize and run
                existing platform.
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <i class="fas fa-chart-line"></i>
              <h4 class="my-3">Performance</h4>
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
header > #find-the-company {
  color: rgb(187, 187, 187);
  height: 50px;
  background: rgb(45, 64, 77);
  display: flex;
  align-items: center;
  .container {
    justify-content: space-between;
    ul > li > i {
      color: white;
    }
  }
}

header > .jumbotron {
  background: black;
  height: 500px;
  position: relative;
  display: flex;
  img {
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
    h1 {
      font-size: 45px;
      color: white;
    }
    p {
      color: rgb(187, 187, 187);
    }
  }
}

#main-menu {
  height: 80px;
  background-color: transparent;
  display: flex;
  align-items: center;
    z-index: 2;
    position: absolute;
    right: 0;
    padding-right: 8%;
  .container {
    justify-content: flex-end;
    align-items: center;
    ul {
      align-items: center;
      li > a {
        color: white;
      }
    }
  }
}

a.link {
  font-weight: bold;
}

header > #company-benefits {
  padding: 60px 0;
  width: 100%;
  background: rgb(236, 235, 235);
  display: flex;
  align-items: center;
  .container {
    display: flex;
    align-items: center;
  }
}

.card {
  min-height: 250px;
  max-height: 380px;
  padding: 30px;
  border-radius: 5px;
  background: white;
  i {
    margin: 0;
    padding: 12.5px;
    color: teal;
    font-size: 25px;
    border-radius: 50%;
    background: rgb(195, 223, 233);
  }
  i:nth-of-type(2) {
    transform: rotate();
  }
  p {
    color: rgb(155, 154, 154);
  }
}

.dots {
  margin: 0;
  padding: 0;
  font-size: 25px;
}
</style>