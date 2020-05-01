<template>
  <div>
    <Header></Header>
    <Nav></Nav>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>
<script>
import  Header from "./Header.vue"
import  Nav from "./Nav.vue"
import  Main from "./Main.vue"
import  Footer from "./Footer.vue"

export default {
  name: "Sccess",
  components: {
    Header,
    Nav,
    Main,
    Footer
  }
};
</script>

<style scopped lang="less">
</style>