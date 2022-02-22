<template>
  <v-container class="d-flex">
    <v-col lg="6">
      <img width="100%" src="../assets/about.jpg" alt="">
    </v-col>
    <v-col lg="6">
      <v-subheader class="text-h4" lg="6">About Us</v-subheader>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad aliquam aut blanditiis dolore dolorem ea expedita
        facilis illum maxime minima nulla officiis perspiciatis quos, recusandae rerum sapiente similique suscipit
        ullam!
      </p>
      <v-list>
        <v-list-item>
          <v-icon color="success" class="mr-3">mdi-check-all</v-icon>
          <v-list-item-subtitle>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab amet architecto
          </v-list-item-subtitle>
        </v-list-item>
        <v-list-item>
          <v-icon color="success" class="mr-3">mdi-check-all</v-icon>
          <v-list-item-subtitle>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab
          </v-list-item-subtitle>
        </v-list-item>
        <v-list-item>
          <v-icon color="success" class="mr-3">mdi-check-all</v-icon>
          <v-list-item-subtitle>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
          </v-list-item-subtitle>
        </v-list-item>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur aut eveniet necessitatibus. Animi
          architecto blanditiis dolores doloribus dolorum eos est, et eum ex, ipsam itaque laborum, nesciunt placeat
          provident quibusdam sit tempore totam unde! Id inventore odit quo totam voluptas!
        </p>
      </v-list>
    </v-col>
  </v-container>
</template>

<script>
export default {
  name: "AboutComponent"
}
</script>