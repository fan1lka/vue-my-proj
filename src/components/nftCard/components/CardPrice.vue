<template>
   
   <div class="card-price"><img src="project-images/eth-logo.svg"/><span>{{ cardPrice }}</span></div>
</template>

<script>
export default {
   name: "CardPrice",

   props: {
      cardPrice: Number,
   }
}
</script>

<style scoped>
   .card-price{
      align-items: center;
      justify-content: center;
      display: flex;
      color: #fff;
      font-weight: 400;
      font-size: 16px;
      margin-bottom: 6px;
      gap: 5px;
   }
   /*  */
</style>