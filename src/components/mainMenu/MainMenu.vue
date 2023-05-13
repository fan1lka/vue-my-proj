<template>
   <section class="section-container">
      <div class="left-side">
      <p class="section-text">NFT is not only judged by appearance but has meaning</p>
      </div>
      <div class="rigth-side">
         <img src="/project-images/section_img.png" class="section-img">
      </div>
   </section>
   <div style="display: flex; align-items: center; justify-content: center;">
      <CardSearch/>
   </div>
   <div>
      <CardFilterList/>
   </div>
   <div class="card-container">
      <NFTCard v-for="nftData in nftDataList" :key="nftData.name" :ntfData="nftData" />
   </div>
</template>

<script>
import NFTCard from "../nftCard/NFTCard.vue";
import CardSearch from '@/components/mainMenu/CardSearch.vue';
import CardFilterList from "@/components/mainMenu/CardFilterList.vue";

export default {
   
   name: "MainMenu",

   components: {
   NFTCard,
   CardSearch,
   CardFilterList,
   },
   data() {
      return {
      nftDataList: [
         {
            imgLink: "project-images/img_1.png",
            name: "Tritology_0001G1",
            price: 0.1,
         },
         {
            imgLink: "project-images/img_2.png",
            name: "Ocean Tree",
            price: 1,
         },
         {
            imgLink: "project-images/img_3.png",
            name: "Element Shape",
            price: 2,
         },
         {
            imgLink: "project-images/img_4.png",
            name: "Coconut Beach",
            price: 1.2,
         },
         {
            imgLink: "project-images/img_5.png",
            name: "Bitcoin Paint",
            price: 2,
         },
         {
            imgLink: "project-images/img_6.png",
            name: "Fragments",
            price: 1.1,
         },
         {
            imgLink: "project-images/img_7.png",
            name: "Aqua Silver",
            price: 1,
         },
         {
            imgLink: "project-images/img_8.png",
            name: "Golden Fragment",
            price: 2,
         },
      ],
      };
   },
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
      width: 1200;
      display: flex;
      justify-content: space-between;
      background: radial-gradient(95.76% 95.76% at 50% 4.24%, #E903C4 24.48%, rgba(76, 0, 199, 0.25) 100%);
      border-radius: 16px;
      margin-top: 120px;
      margin-bottom: 16px;
   }
   .left-side{
      width: 560px;
   }
   .section-text{
      font-weight: 600;
      font-size: 40px;
      /* line-height: 156%; */
      color: #fff;
      margin: 0;
      padding: 24px ;
   }
   .rigth-side{
      position: relative;
   }
   .section-img{
      position: absolute;
      right: 0;
      bottom: 0;
      
   }
   .section-link{
      padding: 12px ;
   }
</style>