<template>
  <div class="search-container">
   <div class="magnify">
      
   </div>
   <input type="text" value="Search">
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
   .search-container{
      display: flex;
      justify-content: center;
      border: solid 1px #FF00D6; 
      border-radius: 16px;
      align-items: center;
      overflow: hidden;
      width: 430px;
      margin-bottom: 35px;
      
   }
   input{
      border: 0;
      outline: none;
      padding: 0;
      line-height: 64px;
      flex: 1;
      width: 100%;
      background-color: #1b0540;
      color: #FF00D6;
   }
   .magnify{
      background-image: url("/public/project-images/search-icon.png");
      width: 24px;
      height: 24px;
      margin: 0 12px;
   }
</style>