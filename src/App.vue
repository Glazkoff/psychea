<template>
  <div id="app">
    <Menu></Menu>

    <router-view />
  </div>
</template>
<script>
import Menu from "@/components/Menu.vue";
export default {
  components: {
    Menu
  }
};
</script>
<style>
@font-face {
  font-family: "Roboto Regular", sans-serif;
  src: url("./assets/Roboto-Regular.ttf") format("truetype");
}
@font-face {
  font-family: "Roboto", sans-serif;
  src: url("./assets/Roboto-Bold.ttf") format("truetype");
}
@font-face {
  font-family: "Roboto Light", sans-serif;
  src: url("./assets/Roboto-Light.ttf") format("truetype");
}

* {
  margin: 0;
  padding: 0;
  font-family: "Roboto Regular", sans-serif;
}
</style>
