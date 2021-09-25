<template>
  <v-app>
    <v-main>
      <div class="main">
        <Header />
        <div class="container">
          <Presentation />
        </div>
        <Footer />
      </div>
    </v-main>
  </v-app>
</template>

<script>
import '../src/assets/styles/master.css';
import '../src/assets/styles/animations.css';
import Header from "./components/Header.vue";
import Presentation from "./components/Presentation";
import Footer from "./components/Footer";

export default {
  name: 'App',
  components:{
    Header,
    Presentation,
    Footer
  }
};
</script>
