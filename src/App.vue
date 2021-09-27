<template>
  <v-app>
    <v-main>
      <div class="main">
        <div class="container">
          <Presentation />
        </div>
        <div class="container">

        </div>
        <Footer />
      </div>
    </v-main>

  </v-app>
</template>

<script>
import '../src/assets/styles/master.css';
import '../src/assets/styles/animations.css';
import Presentation from "./components/Presentation";
import Footer from "./components/Footer";

export default {
  name: 'App',
  components:{
    Presentation,
    Footer
  }
};
</script>
