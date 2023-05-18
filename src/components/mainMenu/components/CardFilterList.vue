<template>
   <ul class="filter-list">
      <li class="filter-item filter-menu" 
         :class="isFiltered ? 'filter-item-selected' : ''"
         @click="setFilter('All')"
      >Filter</li>
      <li v-for="filter in filterMenu" :key="filter"
         class="filter-item"
         :class="selectedFilter == filter ? 'filter-item-selected' : ''"
         @click="setFilter(filter)">
         {{ filter }}</li>
   </ul>
</template>

<script>


export default {
   name: "CardFilterList",

   data() {
      return {
         selectedFilter: "All",
         filterMenu: ["Art", "Games", "Music", "Item", "Character"]
      }
   },

   computed: {
      isFiltered() {
         return this.selectedFilter.toLowerCase() != "all"
      },
   },
      methods: {
      setFilter(filter) {
         this.selectedFilter = filter
         this.$emit("setFilterEmit", filter)
      }
   }
}

</script>

<style scoped>
   ul li,
   ol li {
   list-style: none;
   }
   .filter-list{
      display: flex;
      margin-right: auto;
      margin-left: auto;
      gap: 24px;
   }
   .filter-item{
      color: #fff;
      padding: 8px 24px;
      font-weight: 700;
      font-size: 24px;
      border: solid 1px #FF00D6;
      border-radius: 16px;
      cursor: pointer;
      
   }
   .filter-menu{
      margin-right: 70px;
      
   }
   /* .filter-item:last-child{
      margin-right: auto;
   } */
   .filter-menu::before{
      content: '';
      background-image: url('/public/project-images/filter-icon.svg');
      display: inline-block;
      width: 18px;
      height: 18px;
      margin-right: 11px;
   }

   .filter-item-selected{
      background: radial-gradient(90.7% 279.38% at 94.77% 84.69%, #E903C4 0%, #6100FF 100%)
   }
</style>