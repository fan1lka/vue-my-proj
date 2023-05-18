<template>
  <div style="width: 100%"> 
    <PageStore v-if="!nftInfo" @openNftInfo="openNftInfo"/>
    <PageNftInfo v-if="nftInfo" :nftData="nftInfo" @close="nftInfo = null"/>
  </div>
  
</template>

<script>
import PageStore from './pages/Store.vue';
import PageNftInfo from './pages/NftInfo.vue';
export default {
  name: 'App',

  components: {
    PageStore,
    PageNftInfo
  },
  
  data() {
    return {
      nftInfo: null
    }
  },

  methods: {
    openNftInfo(nftData) {
      this.nftInfo = nftData
      console.log(nftData)
    }
  }
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
