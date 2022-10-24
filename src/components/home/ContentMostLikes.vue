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
                <v-card-text class="panel-trending">
                  <div class="mx-0 my-1 text-subtitle-1">
                      Removing components from the list
                  </div>
                  <div class="mx-0 my-1 grey--text text-subtitle-1 secondaryFont">
                        <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">8</span> 
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">5</span>
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">3</span>
                  </div>
                </v-card-text>
                <!-- --- -->
                <v-card-text class="panel-trending">
                  <div class="mx-0 my-1 text-subtitle-1">
                      Removing components from the list
                  </div>
                  <div class="mx-0 my-1 grey--text text-subtitle-1 secondaryFont">
                        <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">8</span> 
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">5</span>
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">3</span>
                  </div>
                </v-card-text>
                <!-- --- -->
                <v-card-text class="panel-trending">
                  <div class="mx-0 my-1 text-subtitle-1">
                      Removing components from the list
                  </div>
                  <div class="mx-0 my-1 grey--text text-subtitle-1 secondaryFont">
                        <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">8</span> 
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">5</span>
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">3</span>
                  </div>
                </v-card-text>
                <!-- --- -->
                <v-card-text class="panel-trending">
                  <div class="mx-0 my-1 text-subtitle-1">
                      Removing components from the list
                  </div>
                  <div class="mx-0 my-1 grey--text text-subtitle-1 secondaryFont">
                        <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">8</span> 
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">5</span>
                        <span>•</span> 
                        <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">3</span>
                  </div>
                </v-card-text>
                <!-- --- -->
              </v-list>
            </v-sheet>
    </div>
</template>