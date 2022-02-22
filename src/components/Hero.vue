<template>
  <v-container class="pt-15">
    <v-row>
      <v-col lg="6">
        <h2 class="intro-text">Welcome to our Vuetify app</h2>
        <p class="description">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci alias dolorum, eaque fuga quasi ratione
          repellendus repudiandae! Distinctio illo, natus.
        </p>
        <v-btn color="success" class="white--text mr-10" rounded>Get started</v-btn>
        <v-btn color="indigo" class="white--text" rounded><v-icon>mdi-play-circle</v-icon> Watched video</v-btn>
      </v-col>
      <v-col lg="6">
        <img width="100%" src="../assets/hero-img.png" alt="">
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: "HeroComponent"
  }
</script>

<style scoped>
  .intro-text {
    font-size: 60px;
    font-weight: bold;
    font-family: cursive;
    color: #444;
  }
  .description {
    font-size: 19px;
    font-family: cursive;
    margin: 32px 0;
    color: #444444ba;
  }
</style>