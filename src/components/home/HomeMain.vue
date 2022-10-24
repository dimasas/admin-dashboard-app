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
              <KnowledgeBases></KnowledgeBases>
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
  import NavbarMain from "./NavbarMain";
  import KnowledgeBases from "./ContentKnowledgeBases";
  import Trending from "./ContentTrending";
  import MostLikes from "./ContentMostLikes";
  export default {
    components: {
            NavbarMain,
            KnowledgeBases,
            Trending,
            MostLikes,
    },
    data: () => ({
      navLinksLeft: [
        'Article',
      ],
      navLinksRight: [
        'Create Article',
      ],
    }),
  }
</script>