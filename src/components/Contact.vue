<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, nam!</p>
      </v-col>
      <v-col lg="6">
        <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d95837.58129580792!2d69.21591318506022!3d41.353996579096865!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8cb23888afb9%3A0x31c22300affbc36a!2z0K7QvdGD0YHQsNCx0LDQtNGB0LrQuNC5INGA0LDQudC-0L0sINCi0LDRiNC60LXQvdGCLCDQo9C30LHQtdC60LjRgdGC0LDQvQ!5e0!3m2!1sru!2s!4v1645526424306!5m2!1sru!2s"
            width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
      </v-col>
      <v-col lg="6">
        <v-form ref="form">
          <v-text-field
              v-model="name"
              :counter="10"
              label="Name"
              required
          ></v-text-field>

          <v-text-field
              v-model="email"
              label="E-mail"
              required
          ></v-text-field>

          <v-textarea label="Message" v-model="Message"></v-textarea>

          <v-btn color="success" class="mr-4">Send</v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ContactComponent",
  date() {
    return{
      contactInfo:{},
    }
  }
}
</script>

<style scoped>

</style>