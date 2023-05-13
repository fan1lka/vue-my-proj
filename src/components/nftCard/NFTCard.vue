<template>
   <div >
      <div class="card">
         <CardImage :imgLink="ntfData.imgLink"/>
         <CardName :cardTitle="ntfData.name"/>
         <CardPrice :cardPrice="ntfData.price"/>
         <CardButton/>
      </div>
   </div>
</template>

<script>
import CardImage from './components/CardImage.vue';
import CardName from './components/CardName.vue';
import CardPrice from './components/CardPrice.vue';
import CardButton from './components/CardButton.vue';

export default {
   name: "NFTCard",

   components: {
      CardImage,
      CardName,
      CardPrice,
      CardButton,
},

   props: {
      ntfData: null,
   }
}
</script>

<style scoped>
   .card{
      width: 284px;
      height: 380px;
      border: solid 1px #E903C4;
      border-radius: 8px;
      padding-top: 6px;
      text-align: center;
   }

</style>