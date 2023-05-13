<template>
   <div class="store-container">
      <HeaderMenu/>
      <MainMenu/>
   </div>
</template>

<script>

import HeaderMenu from '@/components/headerMenu/HeaderMenu.vue';
import MainMenu from '@/components/mainMenu/MainMenu.vue';

export default {
   name: "PageStore",

   components: {
      HeaderMenu,
      MainMenu,
   },

}
</script>

<style scoped>
   .store-container{
      width: 1200px;
      background-color: #1b0540;
   }
</style>