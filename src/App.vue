<template>
  <v-app>
    <!-- <v-app-bar
      app
      color="transparent"
    >
      <div class="d-flex align-center">
        <v-img
          alt="App Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />
        <v-img
          alt="App Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>
      <v-spacer></v-spacer>
      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar> -->

    <v-main style="padding: 0px !important;">
      <HomeMain/>
      <!-- <Article/> -->
    </v-main>
  </v-app>
</template>

<script>
import HomeMain from './components/home/HomeMain.vue';
// import Article from './components/article/articleMain.vue';

export default {
  name: 'App',

  components: {
    HomeMain,
    // Article,
  },

  data: () => ({
    //
  }),
};
</script>

<style>
    .v-main__wrap{
      background: linear-gradient(94.5deg, #5EAFFF 0%, #007CD6 100%) !important;
      height: 14vh;
    }
    .v-application {
    }
    .v-application--wrap{
      background: #c6e7ff54;
    }
    .v-list {
      padding: 0px !important;
    }
    .primaryFont{
      color:#282B4D !important;
    }
    .secondaryFont{
      color:#8B919F !important;
    }
    .input-search-knowledge{
      height: 5vh !important;
    }
    .btn-createArticle{
      background: linear-gradient(315deg, #1D994E 0.01%, #5EE99E 100%) !important;
      border-radius: 20px !important;
      color: white !important;
    }
    .btn-Question{
      background: linear-gradient(140.58deg, #78C5F1 13.04%, #0C97E4 88%) !important;
      border-radius: 20px !important;
      color: white !important;
    }
    .line-cardSheet{
      border-left-style: solid;
      border-left-width: thick;
    }
    .line-cardSheet.line-orange{
      border-left-color: #F2994A;
    }
    .line-cardSheet.line-red{
      border-left-color: #EB5757;
    }
    .line-cardSheet.line-lightblue{
      border-left-color: #56CCF2;
    }
    .line-cardSheet.line-green{
      border-left-color: #219653;
    }
    .line-cardSheet.line-purple{
      border-left-color: #9B51E0;
    }
    .line-cardSheet.line-blue{
      border-left-color: #2D9CDB;
    }
    /* -- */
    .pt-30{
      padding-top: 30px !important;
    }
    .pt-50{
      padding-top: 50px !important;
    }
    .mt-0{
      margin-top: 0px !important;
    }
    .mt-1{
      margin-top: 1px !important;
    }
    .mt-2{
      margin-top: 2px !important;
    }
    .mt-5{
      margin-top: 5px !important;
    }
    .mt-10{
      margin-top: 10px !important;
    }
    .mr-5{
      margin-right:5px !important;
    }
    /* -- */
    .br-20{
      border-radius: 20px !important;
    }
    .ft-12{
      font-size: 12px !important;
    }
    .ft-13{
      font-size: 13px !important;
    }
    .ft-14{
      font-size: 14px !important;
    }
    .panel-card-knowledge-base{
      padding: 15px !important;
    }
    .panel-trending{
      padding: 2px 16px !important;
    }
    .panel-padding{
      padding: 8px !important;
    }
    .panel-title-knowledge{
      padding: 4px 8px !important;
    }

    @media (min-width: 1264px){
      .container {
          max-width: 1350px;
      }
    }
</style>
