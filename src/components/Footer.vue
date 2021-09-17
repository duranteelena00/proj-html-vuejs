<template>
  <footer>
    <section id="info" class="dark-darkblue">
      <div class="container d-flex">
        <div id="contacts">
          <div class="logo-container">
            <span class="logo"
              ><span class="turquoise pb-2">NEX</span><span>GEN</span></span
            >
          </div>
          <p class="pb-4">
            A Functional HTML Template form Corporate and Business.
          </p>
          <ul>
            <li class="pb-2">
              <i class="fas fa-phone-alt me-2"></i>{{ contacts.number }}
            </li>
            <li class="pb-2">
              <i class="fas fa-envelope me-2"></i>{{ contacts.email }}
            </li>
            <li class="pb-2">
              <i class="fas fa-map-marker-alt me-2"></i>{{ contacts.office }}
            </li>
            <li>
              <button type="button" class="transparent mt-3">
                GET IN TOUCH
              </button>
            </li>
          </ul>
        </div>
        <div class="row">
          <div class="col">
            <div class="card">
              <h3>ABOUT</h3>
              <ul v-for="(link, index) in about" :key="index">
                <li>{{ link }}</li>
              </ul>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <h3>SERVICES</h3>
              <ul v-for="(link, index) in services" :key="index">
                <li>{{ link }}</li>
              </ul>
            </div>
          </div>
          <div class="col">
            <div class="card">
              <h3>SUPPORT</h3>
              <ul v-for="(link, index) in support" :key="index">
                <li>{{ link }}</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div id="copyright">
      <div class="container">
        <p>Enjoy the low price. We are tracking any intention of piracy.</p>
        <p>
          <i class="far fa-copyright"></i>2020 NEXGEN is Proudly Powered by
          <span>Codings</span>.
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    contacts: Object,
    links: Array,
  },
  data() {
    return {
      about: [
        "The Company",
        "Institutional",
        "Social & Events",
        "Innovation",
        "Environment",
        "Technology",
      ],
      services: [
        "Audit & Assurance",
        "Financial Advisory",
        "Analytics M$A",
        "Middle Marketing",
        "Legal Consultant",
        "Regulatory Risk",
      ],
      support: [
        "Responsibility",
        "Terms of Use",
        "About Cookies",
        "Privacy Policy",
        "Accessibility",
        "Information",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#copyright {
  color: rgb(187, 187, 187);
  height: 40px;
  background: rgb(45, 64, 77);
  display: flex;
  align-items: center;
  .container {
    justify-content: space-between;
    p {
      font-size: 12px;
    }
  }
}

#info .card {
  color: rgb(187, 187, 187);
  line-height: 22px;
}

#contacts {
  width: 40%;
}

.row {
  flex-grow: 1;
}
</style>