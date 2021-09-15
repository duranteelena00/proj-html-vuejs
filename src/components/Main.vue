<template>
  <main>
    <section id="about-us">
      <div class="container"></div>
    </section>
    <section id="our-services">
      <div class="container"></div>
    </section>
    <section id="pricing-plans">
      <div class="container"></div>
    </section>
  </main>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      plans: {
        standard: [
          { name: "Standard Accounting", provided: true },
          { name: "Platform Access", provided: true },
          { name: "Business Orientation", provided: false },
          { name: "Dedicated Consultant", provided: false },
          { name: "Personal Assistance", provided: false },
        ],
        Professional: [
          { name: "Standard Accounting", provided: true },
          { name: "Platform Access", provided: true },
          { name: "Business Orientation", provided: true },
          { name: "Dedicated Consultant", provided: false },
          { name: "Personal Assistance", provided: false },
        ],
        ultimate: [
          { name: "Standard Accounting", provided: true },
          { name: "Platform Access", provided: true },
          { name: "Business Orientation", provided: true },
          { name: "Dedicated Consultant", provided: true },
          { name: "Personal Assistance", provided: true },
        ],
      },
    };
  },
};
</script>

<style lang="scss" scoped>
</style>