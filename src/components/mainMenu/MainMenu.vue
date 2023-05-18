<template>
   <section class="section-container">
      <div class="section-body">
         <div class="left-side">
            <p class="section-text">NFT is not only judged by appearance but has meaning</p>
            <a href="#" class="section-link">Join</a>
            <a href="#" class="section-link">Read more</a>
         </div>
         <div class="rigth-side">
            <img src="/project-images/section_img.png" class="section-img">
         </div>
      </div>
   </section>
   <div style="display: flex; align-items: center; justify-content: center;">
      <CardSearch @searchValueEmit="setSearchValue"/>
   </div>
   <div style="display: flex">
      <CardFilterList @setFilterEmit="setFilter"/>
   </div>
   <div class="card-container">
      <NFTCard v-for="nftData in searchValidList" :key="nftData.name" :ntfData="nftData" @buyNft="buyNft(nftData)"/>
   </div>
</template>

<script>
import NFTCard from "../nftCard/NFTCard.vue";
import CardSearch from '@/components/mainMenu/components/CardSearch.vue';
import CardFilterList from "@/components/mainMenu/components/CardFilterList.vue";

export default {
   
   name: "MainMenu",

   components: {
   NFTCard,
   CardSearch,
   CardFilterList,
   },

   data() {
      return {
         nftSortType: "all",
         ntfSortName: "",
         nftDataList: [
            {
               id: 0,
               imgLink: "project-images/img_1.png",
               name: "Tritology_0001G1",
               type: "art",
               price: 0.1,
            },
            {
               id: 1,
               imgLink: "project-images/img_2.png",
               name: "Ocean Tree",
               type: "games",
               price: 1,
            },
            {
               id: 2,
               imgLink: "project-images/img_3.png",
               name: "Element Shape",
               type: "music",
               price: 2,
            },
            {
               id: 3,
               imgLink: "project-images/img_4.png",
               name: "Coconut Beach",
               type: "item",
               price: 1.2,
            },
            {
               id: 4,
               imgLink: "project-images/img_5.png",
               name: "Bitcoin Paint",
               type: "character",
               price: 2,
            },
            {
               id: 5,
               imgLink: "project-images/img_6.png",
               name: "Fragments",
               type: "art",
               price: 1.1,
            },
            {
               id: 6,
               imgLink: "project-images/img_7.png",
               name: "Aqua Silver",
               type: "games",
               price: 1,
            },
            {
               id: 7,
               imgLink: "project-images/img_8.png",
               name: "Golden Fragment",
               type: "music",
               price: 2,
            },
         ],
      };
   },

   computed: {
      filteredNftDataList() {
         if (this.nftSortType.toLowerCase() == "all")
            return this.nftDataList
         else
            return this.nftDataList.filter(nftData => nftData.type.toLowerCase() == this.nftSortType.toLowerCase())
      },
      isFiltered() {
         return this.nftSortType.toLowerCase() != "all"
      },
      searchValidList() {
         return this.filteredNftDataList.filter(nftData => nftData.name.toLowerCase().includes(this.ntfSortName.toLowerCase()))
      }
   },


   methods: {
      setFilter(filter) {
         this.nftSortType = filter
      },
      setSearchValue(searchValue) {
         this.ntfSortName = searchValue
      },
      buyNft(nftData) {
         this.$emit('openNftInfo', nftData)
      }
   }
};
</script >

<style scoped>
   .card-container{
      display: flex;
      flex-wrap: wrap;
      justify-content: center; 
      box-sizing: border-box;
      gap: 10px;
   }
   .section-container{
      display: flex;
      justify-content: center;
   }
   .section-body{
      width: 80%;
      display: flex;
      justify-content: space-between;
      background: radial-gradient(95.76% 95.76% at 50% 4.24%, #E903C4 24.48%, rgba(76, 0, 199, 0.25) 100%);
      border-radius: 16px;
      margin-top: 66px;
      margin-bottom: 16px;
      padding: 24px 0 26px 42px;
   }
   .left-side{
      width: 600px;
   }
   .section-text{
      font-weight: 600;
      font-size: 40px;
      line-height: 156%;
      color: #fff;
      margin: 0;
      /* padding: 24px ; */
      margin-bottom: 36px;
   }
   .rigth-side{
      position: relative;
   }
   .section-img{
      position: absolute;
      right: 0;
      top: -98.5px;
      
   }
   .section-link{
      padding: 8px 24px;
      background: radial-gradient(95.76% 95.76% at 50% 4.24%, #E903C4 24.48%, rgba(76, 0, 199, 0.25) 100%);
      border-radius: 16px;
      color: #fff;
      text-decoration: none;
      font-weight: 700;
      font-size: 24px;
      line-height: 33px;
      margin-right: 16px;
      transition: 0.8s;
   }
   .section-link:hover{
      color: aqua;
   }
</style>