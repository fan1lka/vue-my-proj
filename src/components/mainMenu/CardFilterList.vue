<template>
   <ul class="filter-list">
      <li class="filter-item filter-menu">Filter</li>
      <li class="filter-item">Art</li>
      <li class="filter-item">Games</li>
      <li class="filter-item">Music</li>
      <li class="filter-item">Item</li>
      <li class="filter-item">Character</li>
   </ul>
</template>

<script>
export default {

   name: "CardFilterList",
}
</script>

<style scoped>
   ul li,
   ol li {
   list-style: none;
   }
   .filter-list{
      display: flex;
      justify-content: center;
      gap: 24px;
   }
   .filter-item{
      color: #fff;
      padding: 8px 24px;
      font-weight: 700;
      font-size: 24px;
      border: solid 1px #FF00D6;
      border-radius: 16px;
   }
   .filter-menu{
      margin-right: auto;
   }
   .filter-item:last-child{
      margin-right: auto;
   }
   .filter-menu::before{
      content: '';
      background-image: url('/public/project-images/filter-icon.svg');
      display: inline-block;
      width: 18px;
      height: 18px;
      margin-right: 11px;
   }
</style>