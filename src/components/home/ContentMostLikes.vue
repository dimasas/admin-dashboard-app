<template>
    <div>
            <v-card-title class="panel-padding">
              <v-img
                alt="App Logo"
                class="shrink mr-2"
                contain
                src="../../assets/sectionLogo-Like.svg"
                transition="scale-transition"
                width="20"
              />
              <h4>Most Like</h4>
            </v-card-title>
            <v-sheet rounded="lg" color="transparent"
              min-height="18vh"
              max-height="32vh"
              elevation="0"
              style="overflow-y: scroll;overflow-x: hidden;">
              <v-list color="transparent">
                <v-card-text class="panel-trending" v-for="data in this.mostLikes" :key="data.id">
                  <div class="mx-0 my-1 text-subtitle-1">
                     {{ data.wiki.space.name }} >> {{ data.wiki.name }} >> {{ data.name }}
                  </div>
                  <div class="mx-0 my-1 grey--text text-subtitle-1 secondaryFont">
                        <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">{{ data.likes_count }}</span> 
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">{{ data.total_view }}</span>
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">{{ data.comments_count }}</span>
                  </div>
                </v-card-text>
              </v-list>
            </v-sheet>
    </div>
</template>

<script>
  export default {
    props : ["mostLikes"],
  }
</script>