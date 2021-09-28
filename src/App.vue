<template>
  <v-app>
    <v-main>
      <div class="main">
        <div class="container" v-if="$router.currentRoute.path === '/'">
          <Presentation />
          <div class="portfolioItemContainer">
            <a class="portfolioItem"
               v-for="item in portfolioItems"
               :key="item.title"
               v-bind:style="{animation: ((portfolioItems.indexOf(item)+1)/portfolioItems.length)*2 + 's popFromNothing'}"
               @click="$router.push(item.link)">{{item.title}}</a>
          </div>
        </div>
        <div v-if="this.$router.currentRoute.path !== '/'">
          <a class="backButton" @click="goBack">Back</a>
        </div>
        <router-view class="test"/>
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
    Footer,
  },
  data: function(){
    return{
      portfolioItems:[
        {title:"CV",link:"/CV"},
        {title:"CV",link:"/CV"},
        {title:"CV",link:"/CV"},
      ],
    }
  },
  methods: {
    goBack() {
      this.$router.push('/');
    }
  }
};
</script>
