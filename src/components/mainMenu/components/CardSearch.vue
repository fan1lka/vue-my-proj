<template>
  <div class="search-container">
   <div class="magnify">
      
   </div>
   <input v-model="searchValue" type="text" placeholder="Search" @input="setSearchValue()" >
  </div>
</template>

<script>
export default {
   data(){
      return{
         searchValue: "",
         
      }
   },
   methods: {
      setSearchValue(){
         this.$emit("searchValueEmit", this.searchValue)
      }
   }
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
   ::-webkit-input-placeholder {
      color:#FF00D6;
   }
   ::-moz-placeholder {
      color:#FF00D6;
   }/* Firefox 19+ */
   :-moz-placeholder {
      color:#FF00D6;
   }/* Firefox 18- */
   :-ms-input-placeholder {
      color:#FF00D6;
      }
</style>