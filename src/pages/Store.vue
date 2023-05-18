<template>
   <div class="store-container">
      <HeaderMenu/>
      <MainMenu @openNftInfo="openNftInfo"/>
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
   methods: {
      openNftInfo(nftData) {
         this.$emit('openNftInfo', nftData)
      }
   },
}
</script>

<style scoped>
   .store-container{
      background-color: #1b0540;
      /* max-width: 1200px; */
      width: 100%;
   }
</style>