<template>
  <div class="layout">
    <header class="header">
      <Navbar />
    </header>
    <slot/>
    <Footer></Footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Navbar from '~/components/Navbar.vue';
import Footer from "../components/Footer";

export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style lang="scss" scoped>
body {
  margin:0;
  padding:0;
  line-height: 1.5;
  border-top: 4px solid #5a67d8;
  font-size: $base-font-size;
}

.layout {
  max-width: 860px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.nav__link {
  margin-left: 20px;
}
</style>
