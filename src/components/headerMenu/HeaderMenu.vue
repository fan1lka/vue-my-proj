<template>
   <header class="header">
      <img src="/project-images/bitcoin.png" class="header-logo">
      <div class="header-container">
         
         <ul class="header-list">
            <li class="header-item"><a href="#" class="header-link">Create</a></li>
            <li class="header-item"><a href="#" class="header-link">Store</a></li>
            <li class="header-item"><a href="#" class="header-link">Categories</a></li>
            <li class="header-item"><a href="#" class="header-link">Favorite</a></li>
            <li class="header-item"><a href="#" class="header-link">Explore</a></li>
            <a href="#" class="notification"></a>
         </ul>
         
      </div>
      <!-- <a href="#" class="avatar"></a> -->
      <img src="/project-images/avatar.png" class="avatar">
   </header>
</template>

<script>
export default {
   name: "HeaderMenu",
}
</script>

<style scoped>
   .header{
      display: flex;
   }
   .header-container{
      display: flex;
      /* margin-bottom: 51px; */
      display: flex;
      width: 100%;
   }
   ul li,
   ol li {
   list-style: none;
   }
   .header-list{
      display: flex;
      justify-content: center;
      margin: 0;
      gap: 56px;
      background: linear-gradient(180deg, #4C00C7 0%, #E903C4 100%);
      border-radius: 0px 0px 16px 16px;
      padding-right: 43px;
      width: 100%;
      margin-left: 18px;
      margin-right: 40px;
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
   .header-logo{
      width: 120px;
      height: 68px;
      margin-top: 17px;
      margin-left: auto;
   }
   .avatar{
      width: 72px;
      height: 72px;
      margin-top: 22px;
      padding-right: 32px;
      cursor: pointer;
   }
   .notification{
      background-image: url("/public/project-images/notification.png");
      width: 35px;
      height: 40px;
      align-self: center;
   }
</style>