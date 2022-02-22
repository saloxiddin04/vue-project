<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Projects</v-subheader>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam, similique!</p>
      </v-col>
      <v-col lg="4" v-for="project in 3" :key="project">
        <v-card class="mx-auto my-12" max-width="374">
          <v-img height="250"
                 src="https://images.pexels.com/photos/374016/pexels-photo-374016.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940"></v-img>
          <v-card-title>Web Development</v-card-title>
          <v-card-text>
            <div>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur deleniti dolore ducimus enim esse
            </div>
            <v-divider class="my-5"></v-divider>
            <v-card-actions>
              <v-btn class="success" rounded>View Details</v-btn>
              <v-spacer/>
              <v-rating
                  :value="4.5"
                  color="amber"
                  dense
                  half-increments
                  readonly
                  size="14"
              ></v-rating>
            </v-card-actions>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ProjectComponent"
}
</script>