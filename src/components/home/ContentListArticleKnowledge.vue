<template>
  <div>
    <v-card-title class="panel-padding">
      <v-img
        alt="App Logo"
        class="shrink mr-2"
        contain
        src="../../assets/sectionLogo-Knowledge.svg"
        transition="scale-transition"
        width="40"
      />
      <h4>Knowledge Bases</h4>
    </v-card-title>
    <v-sheet
      min-height="60vh"
      max-height="70vh"
      rounded="lg"
      elevation="0"
      color="transparent"
      class="panel-card-knowledge-base"
      style="overflow-y: scroll; overflow-x: hidden"
    >
      <!-- baru -->
      <v-row>
          <v-col cols="12">
            <v-sheet rounded="lg">
              <v-list color="transparent">
                <v-list-item color="lighten-4">
                  <v-row class="my-0">
                    <v-col cols="12">
                      <v-card-title class="panel-title-knowledge">
                        <h4>
                          Removing component from the chasis
                        </h4>
                      </v-card-title>
                      <v-card-subtitle class="panel-title-knowledge my-0">
                        <div id="date" class="secondaryFont">11 Oktober 2022 11:16</div>
                      </v-card-subtitle>
                    </v-col>
                  </v-row>
                </v-list-item>
                <v-list-item color="grey lighten-4">
                  <v-row class="text-subtitle-3 secondaryFont my-3">
                      <v-col cols="7">
                              <v-btn icon><v-icon size="14" light>mdi-heart</v-icon></v-btn><span id="count-likes">8</span> 
                              <span>•</span> 
                              <v-btn icon><v-icon size="14" light>mdi-eye</v-icon></v-btn><span id="count-views">5</span>
                              <span>•</span> 
                              <v-btn icon><v-icon size="14" light>mdi-comment</v-icon></v-btn><span id="count-comments">3</span>    
                      </v-col>
                      <v-col cols="5" class="align-end">
                          <div class="mx-0 grey--text text-subtitle-1 secondaryFont">                                            
                              <v-btn
                                  text
                                  small
                                  right
                                  color="primary"
                                  class="secondaryFont ml-5"
                                  >
                                  Lihat Article
                              </v-btn>
                          </div> 
                      </v-col>
                    </v-row>
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>
      </v-row>
      <!-- baru -->
    </v-sheet>
  </div>
</template>

<script>

export default{
  props: ['knowledgeBases'],
  data() {
    return {
      color : [
        "orange",
        "red",
        "lightblue",
        "blue",
        "green"
      ],
    }
  },
  created() {
    // this.randomColor()
  },
  methods:{
    randomColor() {
      let color = "line-cardSheet line-" + this.color[Math.floor(Math.random()*this.color.length)];
      return color
    }
  }
}
</script>
