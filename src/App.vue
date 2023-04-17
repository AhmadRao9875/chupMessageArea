<template>
  <secondryNav />
  <!-- <uploadFile /> -->
  <!-- <forwardMessage /> -->
  <HelloWorld />
</template>

<script>
import secondryNav from './components/secondryNav.vue';
// import uploadFile from './components/uploadFile.vue';
import HelloWorld from "./components/HelloWorld.vue";
// import forwardMessage from "./components/forwardMessage.vue";


export default {
  name: "App",
  components: {
    secondryNav,
    HelloWorld,
    // forwardMessage,
    // uploadFile,
  },
};
</script>

<style></style>
