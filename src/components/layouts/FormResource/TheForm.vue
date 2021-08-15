<template>
  <div class="contact-container">
    <!--contact infotmation-->
    <contact-guide>
      <template #title>
        Contact Information
      </template>
      <template #description>
        Fill up the form and our Team will get back to you within 24 hours
      </template>
    </contact-guide>
    <!--user input form-->
    <form-control></form-control>
    
  </div>
</template>

<script>
import ContactGuide from "./TheContactGuide.vue";
import FormControl from './TheFormControl.vue';
export default {
  components: {
    ContactGuide,
    FormControl
  },
};
</script>

<style scoped>
div.contact-container {
  display: flex;
  flex-direction: row;
  width: 1000px;
  margin: 10rem auto;
  box-shadow: 0 2px 10px 2px rgb(216, 216, 216);
  border-radius: 10px;
  background-color: white;
}
</style>
