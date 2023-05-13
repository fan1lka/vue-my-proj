<template>
  <div>
    <!-- <NFTCard v-for="nftData in nftDataList" :key="nftData.name" :ntfData="nftData"/> -->
    <PageStore/>
  </div>
  
</template>

<script>
// import NFTCard from './components/nftCard/NFTCard.vue';
import PageStore from './pages/Store.vue';

export default {
  name: 'App',

  components: {
    PageStore,
    // NFTCard,
  },
  
  
}
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
