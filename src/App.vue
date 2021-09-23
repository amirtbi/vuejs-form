<template>
  <the-header></the-header>
  <the-form></the-form>
</template>

<script>
import TheForm from "./components/layouts/FormResource/TheForm.vue";
import TheHeader from "./components/layouts/TheHeader.vue";
export default {
  components: {
    TheForm,
    TheHeader,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@1,300&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;1,300&display=swap");

:root {
  --primaryColor: rgb(84, 5, 175);
  --secondaryColor: rgb(182, 181, 181);
  --accentColor: pink;
  --primaryBubbleColor: #f3adb9;
  --secondaryBubbleColor: rgba(53, 74, 189, 0.7);
}
html,
body {
  margin: 0;
  padding: 0;
  font-family: "Roboto", sans-serif;
}

* {
  box-sizing: border-box;
}
</style>
