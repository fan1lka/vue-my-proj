<template>
   <header class="header-container">
         <ul class="header-list">
         <li class="header-item"><a href="#" class="header-link">Create</a></li>
         <li class="header-item"><a href="#" class="header-link">Store</a></li>
         <li class="header-item"><a href="#" class="header-link">Categories</a></li>
         <li class="header-item"><a href="#" class="header-link">Favorite</a></li>
         <li class="header-item"><a href="#" class="header-link">Explore</a></li>
      </ul>
   </header>
</template>

<script>
export default {
   name: "HeaderMenu",
}
</script>

<style scoped>
   .header-container{
      width: 1150px;
      margin-bottom: 51px;
      margin: 0 auto;
   }
   ul li,
   ol li {
   list-style: none;
   }
   .header-list{
      display: flex;
      justify-content: center;
      margin: 0 auto;
      gap: 56px;
      height: 105px;
      background: linear-gradient(180deg, #4C00C7 0%, #E903C4 100%);
      border-radius: 0px 0px 16px 16px;
      
   }
   .header-item{
      align-self: center;
      font-weight: 700;
      font-size: 24px;
      line-height: 33px
   }
   .header-link{
      text-decoration: none;
      color: #fff;
      transition: 0.8s;
   }
   .header-link:hover{
      color: aqua;
   }
</style>