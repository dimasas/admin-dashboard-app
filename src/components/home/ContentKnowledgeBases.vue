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
      
      <v-row>
          <v-col cols="4" v-for="data in this.knowledgeBases" :key="data.id" style="height:auto">
            <v-sheet rounded="lg" :class="randomColor()">
              <v-list color="transparent">
                <v-card-text class="panel-padding">
                  <div class="mx-0 my-1">
                    <v-card-title class="panel-title-knowledge">
                      <h4>
                        {{ data.name }}
                      </h4>
                    </v-card-title>
                  </div>
                </v-card-text>
                <v-list-item color="grey lighten-4">
                  <v-row no-gutters class="footer-bases">
                    <!-- <v-col>
                      <v-card solo flat class="pa-2">
                        0 <span class="ft-14 secondaryFont">Question(s)</span>
                      </v-card>
                    </v-col> -->
                    <v-col>
                      <v-card solo flat class="pa-2">
                        {{ data.wikis.length }} <span class="ft-14 secondaryFont">Article(s)</span>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>
      </v-row>
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
