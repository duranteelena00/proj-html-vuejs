<template>
  <main>
    <section id="about-the-company">
      <img class="dots" src="@/assets/img/dots.png" alt="" />
      <div class="container">
        <div class="text pb-4">
          <h4>ABOUT THE NETWORK</h4>
          <h2 class="py-3">
            <span class="turquoise py-1 px-2">The</span> Company
          </h2>
          <p>
            For 12 years we have been providing audit and warranty,financial
            advice, risk advice, taxes and related services to selected clients.
          </p>
        </div>
        <div class="cards-container">
          <div class="row py-4">
            <div class="col">
              <div class="card p-0">
                <h3 class="pb-3">Tradition <i class="fas fa-award ms-2"></i></h3>
                
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
              </div>
            </div>
            <div class="col">
              <div class="card p-0">
                <h3 class="pb-3">Security<i class="fas fa-lock ms-3"></i></h3>
                
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
              </div>
            </div>
          </div>
          <div class="row py-4">
            <div class="col">
              <div class="card p-0">
                <h3 class="pb-3">
                  Certificate<i class="far fa-edit ms-3"></i>
                </h3>
                
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
              </div>
            </div>
            <div class="col">
              <div class="card p-0">
                
                <h3 class="pb-3">
                  Expertise<i class="fas fa-graduation-cap ms-3"></i>
                </h3>
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <img class="about" src="@/assets/img/about-3.jpg" alt="" />
    </section>
    <section id="company-services" class="dark-darkblue">
      <img class="dots" src="@/assets/img/dots.png" alt="" />
      <div class="container">
        <div class="text pb-3">
          <h4>OUR BUSINESS AREA</h4>
          <h2 class="py-4">
            Excellence in <span class="turquoise py-1 px-2">Services</span>
          </h2>
          <p>
            We are leaders in providing consultancy services with a set of
            cutting-edge technologies and a team of experiences and renewed
            professionals. This are some options that you can hire.
          </p>
        </div>
        <div class="row py-5">
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-network-wired"></i>
              <h3 class="my-3">Audit & Assurance</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-briefcase"></i>
              <h3 class="my-3">Financial Advisory</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-chart-bar"></i>
              <h3 class="my-3">Analytics and M&A</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
        </div>
        <div class="row py-5">
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-plane"></i>
              <h3 class="my-3">Middle Marketing</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-globe-americas"></i>
              <h3 class="my-3">Legal Consulting</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
          <div class="col">
            <div class="card p-0">
              <i class="fas fa-inbox"></i>
              <h3 class="my-3">Regulatory Risk</h3>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              <button class="transparent mt-4">READ MORE</button>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="pricing-plans" class="light-turquoise">
      <div class="container">
        <div class="text pb-3">
          <h4>MONTHLY PLANS</h4>
          <h2 class="py-4">
            <span class="turquoise py-1 px-2">Pricing</span>Table
          </h2>
          <p>
            We can help you deliver and execute your future, wherever you
            compete, using the latest technologies, from strategy development to
            implementation.
          </p>
        </div>
        <div class="row py-4">
          <div class="col" v-for="(plan, index) in plans" :key="index">
            <div class="card">
              <div class="text-center">
                <i class="icon pb-3" :class="plan.icon"></i>
                <h3 class="pb-4">{{ plan.name }}</h3>
                <p class="h3 pb-4">{{ plan.price }}</p>
              </div>
              <ul>
                <li>
                  Standard Accounting
                  <i class="fas" :class="plan.standardAccounting"></i>
                </li>
                <li>
                  Platform Access
                  <i class="fas" :class="plan.platformAccess"></i>
                </li>
                <li>
                  Business Orientation
                  <i class="fas" :class="plan.businessOrientation"></i>
                </li>
                <li>
                  Dedicated Consultant
                  <i class="fas" :class="plan.dedicatedConsultant"></i>
                </li>
                <li>
                  Personal Assistance
                  <i class="fas" :class="plan.personalAssistance"></i>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      plans: [
        {
          name: "Standard",
          price: "$490/mo",
          icon: "fas fa-rocket",
          standardAccounting: "fa-check",
          platformAccess: "fa-check",
          businessOrientation: "fa-times",
          dedicatedConsultant: "fa-times",
          personalAssistance: "fa-times",
        },
        {
          name: "Professional",
          price: "$890/mo",
          icon: "fas fa-briefcase",
          standardAccounting: "fa-check",
          platformAccess: "fa-check",
          businessOrientation: "fa-check",
          dedicatedConsultant: "fa-times",
          personalAssistance: "fa-times",
        },
        {
          name: "Ultimate",
          price: "$1390/mo",
          icon: "far fa-gem",
          standardAccounting: "fa-check",
          platformAccess: "fa-check",
          businessOrientation: "fa-check",
          dedicatedConsultant: "fa-check",
          personalAssistance: "fa-check",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#about-the-company {
  position: relative;
  img.about {
    width: 50%;
    height: 100%;
    object-fit: cover;
    object-position: top;
    position: absolute;
    top: 0;
    right: 0;
  }
  .container {
    flex-direction: column;
    .cards-container {
      width: 50%;
      padding-right: 65px;
    }
  }
  .text > p {
    color: rgb(148, 147, 147);
  }
  .row {
    flex-direction: row;
  }
  .card > p {
    color: rgb(148, 147, 147);
  }
}

#company-services {
  position: relative;
  .container {
    flex-direction: column;
  }
}

#company-services i {
  font-size: 30px;
  justify-content: flex-start;
}

#company-services .text > h2 > span.turquoise {
  background: rgb(14, 39, 45);
}

#pricing-plans > .container {
  flex-direction: column;
}

#pricing-plans .text {
  text-align: center;
}

#pricing-plans .card {
  background: white;
}

.card .text-center {
  text-align: center;
}

.card i.icon {
  font-size: 30px;
  text-align: center;
}

.card .h3 {
  color: #038483;
  font-size: 30px;
  font-weight: 600;
}
.card > ul {
  font-size: 14px;
  line-height: 22px;
  color: rgb(148, 147, 147);
}

#pricing-plans .card i:not(i.icon) {
  float: right;
}
</style>