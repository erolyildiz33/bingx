<template>
    <Popper arrow placement="bottom" >
    <button>Filitre</button>
    <template #content>
      <div ><Filtre /></div>
    </template>
  </Popper>
  </template>
  
  <script>
    import { defineComponent } from "vue";
    import Popper from "vue3-popper";
    import Filtre from "./filtre.vue";
  
    export default defineComponent({
      components: {
        Popper,
        Filtre
      },
    });
  </script>
  <style >
   
    :root {
      --popper-theme-background-color: #333333;
      --popper-theme-background-color-hover: #333333;
      --popper-theme-text-color: #ffffff;
      --popper-theme-border-width: 0px;
      --popper-theme-border-style: solid;
      --popper-theme-border-radius: 6px;
      --popper-theme-padding: 32px;
      --popper-theme-box-shadow: 0 6px 30px -6px rgba(0, 0, 0, 0.25);
      --poppover-theme-width:750px;
     

    }
    </style>
    <style scoped>
    :deep(.popper) {
    width: max-content;
   
    }
    </style>
  