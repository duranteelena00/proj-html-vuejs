<template>
  <section>
    <footer id="info">
      <div class="container"></div>
    </footer>
    <footer id="copyright">
      <div class="container"></div>
    </footer>
  </section>
</template>

<script>
export default {
  name: "Footer",
  data(){
      return {    
        info: {
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
        },
      }
  }
};
</script>

<style lang="scss" scoped>
</style>