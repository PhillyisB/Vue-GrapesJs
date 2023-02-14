<template>
  <div class="container">
    <div id="gjs">
    </div>
  </div>
</template>

<script>
const grapesjs = require("grapesjs"); // can be replaced with the es6 import if a transpiler like babel is used
require("grapesjs/dist/css/grapes.min.css");
require("grapesjs-mjml"); // this is a plugin for grapes js > https://github.com/artf/grapesjs-blocks-basic

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  mounted(){
    // grapesjs equals the grapesjs from the first require line
    grapesjs.init({
      container: '#gjs',
      plugins: [
       'gjs-mjml'
      ]
    })
  }
};
</script>

<style scoped src="grapesjs/dist/css/grapes.min.css">
  /* global styles */
</style>

