<template>
   <div class="container d-block border py-3 my-3">
        
        <Popover />
    </div>

 
</template>

<script>
import Popover from "./components/popover.vue";
export default {
  name: "app",
  components: {
    Popover
  }
};
</script>

<style>
#app {

  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  top: 0px;
  position:absolute;
  width: 100%;
  left: 0;
  right: 0;
}
</style>
