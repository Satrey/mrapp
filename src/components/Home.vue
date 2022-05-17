<template>
  <v-container>
    <h1 v-text="message" class="text-center mt-4"  ></h1>
    <v-btn @click="showMessage()" color="primary">Send</v-btn>
  </v-container>
</template>
<script>
export default {
  name: 'HomeComponent',

  data: () => {
    return{
      message: 'This is an message for New home page Title!',
      status: 'New',
    }
  },
  computed: {

  },
  methods: {
    showMessage() {
      if (this.status == 'Old') {
        this.message = 'This is an message for New home page Title!'
        this.status = 'New'
      } else {
        this.message = 'This is an message for Old home page Title!'
        this.status = 'Old'
      }
    },
  },
}
</script>
<style>
  
</style>
