<template>
  <HeaderMenu/>
  <img src="/project-images/arrow.png" class="arrow" @click="$emit('close')">
  <NftFullCard :nftData="nftData"/>
</template>

<script>
import HeaderMenu from '@/components/headerMenu/HeaderMenu.vue';
import NftFullCard from '@/components/nftCard/NftFullCard.vue';

export default {
    name: "NftInfo",

    components: {
    HeaderMenu,
    NftFullCard,
    },

    props: {
      nftData: null
    }
}
</script>

<style scoped>
  .arrow{
    margin-top: 11px;
    margin-left: 40px;
    margin-bottom: 26px;
    cursor: pointer;
  }
</style>