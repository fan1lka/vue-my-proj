<template>
  <div class="card-title">{{ cardTitle }}</div>
</template>

<script>
export default {
   name: "CardName",

   props: {
      cardTitle: String,
   }
}
</script>

<style scoped>
   .card-title{
      margin-top:22px;
      color: #fff;
      margin-bottom: 4px;
      font-weight: 700;
      font-size: 20px;
   }
</style>