<template>
   <div>
      <img :src="imgLink" class="card-img">
   </div>
</template>

<script>
export default {
   name: "CardImage",

   props: {
      imgLink: String,
   }
}
</script>

<style scoped>
   
</style>