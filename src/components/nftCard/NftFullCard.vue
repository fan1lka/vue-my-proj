<template>
   <div class="card-info-container">
      <div class="card-info">
         <img :src="nftData.imgLink" class="card-info-img">
         <p class="card-info-title">{{nftData.name}}</p>
         <p class="card-info-text">Golden Fragment NFT is a clear metal that has gold flakes. This color is a powder coat polyester top coat and has a glossy finish</p>
         <p class="card-info-price"><img src="/project-images/rhomb.png"/><span>{{nftData.price}}</span></p>
         <button class="card-info-btn">Buy</button>
      </div>
   </div>
</template>

<script>
export default {
   name: "NftFullCard",

   props: {
      nftData: null
   }
}
</script>

<style scoped>
   .card-info-container{
      min-width: 1050px;
      box-sizing: border-box;
      margin: 0 auto;
      padding: 25px;
   }
   .card-info{
      display: flex;
      flex-direction: column;
      align-items: center;
   }
   .card-info-img{
      min-width: 800px;
      max-width: 1300px;
      height: 570px;
      margin-bottom: 16px;
   }
   .card-info-title{
      max-width: 1000px;
      font-weight: 700;
      font-size: 50px;
      margin: 0;
      background: linear-gradient(180deg, #E903C4 0%, #6100FF 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
   }
   .card-info-text{
      min-width: 1000px;
      width: 100%;
      max-width: 1300px;
      font-weight: 400;
      font-size: 40px;
      margin-top: 16px;
      text-align: center;
      color: #fff;
   }
   .card-info-price{
      display: flex;
      align-items: center;
      font-weight: 400;
      font-size: 64px;
      color: #fff;
      margin: 0;
      gap: 10px;
      margin-bottom: 24px;
   }
   
   .card-info-btn{
      min-width: 1000px;
      width: 100%;
      max-width: 1300px;
      padding: 25px 464px;
      font-weight: 800;
      font-size: 64px;
      color: #fff;
      background: linear-gradient(180deg, #E903C4 0%, #6100FF 100%, rgba(255, 255, 255, 0) 100%);
      filter: drop-shadow(0px 4px 0px #FFFFFF);
      border-radius: 16px;
      margin-bottom: 100px;
      cursor: pointer;
   }
</style>