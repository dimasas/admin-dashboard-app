<template>
    <div>
        <v-row
          min-width="360"
          min-height="40"
          align-center
          class="mt-2">
            <v-col cols="6" class="d-flex">
                <v-btn text>
                    <v-icon dark> mdi-home</v-icon> Normal
                </v-btn>
            </v-col>
            <v-col cols="6" class="d-flex flex-row-reverse">
                <v-btn
                    rounded
                    class="btn-postQuestion"
                    v-for="navLinksRight in navLinksRight"
                    :key="navLinksRight"
                    text
                    >
                    {{ navLinksRight }}
                </v-btn>
                <!-- <v-btn
                    rounded
                    outlined
                    color="white"
                    class="mr-5"
                    >
                    Create Article
                </v-btn> -->
            </v-col>
        </v-row> 
    </div>
</template>


<script>
  export default {
    data: () => ({
      // navLinksLeft: [
      //   'Article',
      // ],
      navLinksRight: [
        'Post Question'
      ],
    }),
  }
</script>