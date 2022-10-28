<template>
  <div>
    <Header/>
    <Nuxt />
   <Footer/>
  </div>
</template>
<script>
import Header from "../components/header-footer/Header";
import Footer from "../components/header-footer/Footer";
export default {
  components: {Footer, Header}
}
</script>
