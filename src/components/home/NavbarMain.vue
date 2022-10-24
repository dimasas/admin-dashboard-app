<template>
    <div>
        <v-row
          min-width="360"
          min-height="40"
          align-center
          class="mt-2">
            <v-col cols="6" class="d-flex">
              <v-img
                alt="App Logo"
                class="shrink mr-2"
                contain
                src="../../assets/logoJasnita.svg"
                transition="scale-transition"
                width="140"
              />
            </v-col>
            <v-col cols="6" class="d-flex flex-row-reverse">
              <v-btn
                rounded
                class="btn-createArticle"
                v-for="navLinksRight in navLinksRight"
                :key="navLinksRight"
                text
              >
                {{ navLinksRight }}
              </v-btn>
            </v-col>
        </v-row> 
    </div>
</template>


<script>
  export default {
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