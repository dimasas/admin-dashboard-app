<template>
    <v-app id="inspire">
      <v-main class="greylighten-3">
        <v-container>
          <!-- -- -->
          <NavbarPage></NavbarPage>
          <!-- -- -->
          <v-row>
            <v-col cols="9" min-height="70vh"
                rounded="lg"
                elevation="0"
                class="panel-card-knowledge-base">
                <!-- -- -->
                <ContentArticle></ContentArticle>
                <!-- -- -->
            </v-col>
            <v-col cols="3">
              <!-- -- -->
              <MostLikes></MostLikes>
              <!-- -- -->
              <Trending></Trending>
              <!-- -- -->
            </v-col>
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </template>
  
  <script>
    import NavbarPage from "./NavbarPage";
    import ContentArticle from "./ContentArticle.vue";
    export default {
      components: {
    NavbarPage,
    ContentArticle
},
      data: () => ({
        navLinksLeft: [
          'Article',
        ],
        navLinksRight: [
          'Publish',
        ],
      }),
    }
  </script>