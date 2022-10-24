<template>
  <v-app id="inspire">
    <v-main class="greylighten-3">
      <v-container>
        <!-- -- -->
        <NavbarMain></NavbarMain>
        <!-- -- -->
        <v-row justify="center" min-width="360" class="mt-0">
          <v-col cols="12" sm="6">
            <v-text-field
              v-model="message2"
              solo
              label="Search what you need here"
              prepend-inner-icon="mdi-magnify"
              flat
              clearable
              class="br-20 input-search-knowledge"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="9" min-height="70vh"
              rounded="lg"
              elevation="0"
              class="panel-card-knowledge-base">
              <!-- -- -->
              <KnowledgeBases :knowledgeBases="this.knowledgeBases"></KnowledgeBases>
              <!-- -- -->
          </v-col>
          <v-col cols="3">
            <!-- -- -->
            <MostLikes :mostLikes="this.mostLikes"></MostLikes>
            <!-- -- -->
            <Trending :trending="this.trending"></Trending>
            <!-- -- -->
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  import NavbarMain from "./NavbarMain";
  import KnowledgeBases from "./ContentKnowledgeBases";
  import Trending from "./ContentTrending";
  import MostLikes from "./ContentMostLikes";
  import axios from 'axios';

  export default {
    components: {
      NavbarMain,
      KnowledgeBases,
      Trending,
      MostLikes,
    },
    data() {
      return {
        navLinksLeft: [
          'Article',
        ],
        navLinksRight: [
          'Create Article',
        ],
        knowledgeBases: null,
        trending: null,
        mostLikes: null
      }
    },
    created() {
      this.getDataDashboard();
    },
    methods: {
      getTeamSLug() {
        return location.search.split('team=')[1];
      },
      getDataDashboard() {
        let teamSlug = this.getTeamSLug();
        axios.get(`http://opus.bona.dev.jasmeet.id/api/dashboard/${teamSlug}`)
          .then(
            response => (
              this.knowledgeBases = response.data.data.knowledgeBases.spaces,
              this.trending = response.data.data.pageTrending,
              this.mostLikes = response.data.data.mostLikes
            )
          )
      }
    },
  }
</script>