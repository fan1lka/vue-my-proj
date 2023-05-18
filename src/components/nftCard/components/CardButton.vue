<template>
  <button class="card-btn">Buy</button>
</template>

<script>
export default {
    name: "CardButton",

}
</script>

<style scoped>
    .card-btn{
      padding: 8px 96px;
      background: linear-gradient(180deg, #E903C4 0%, #6100FF 100%, rgba(255, 255, 255, 0) 100%);
      border-radius: 8px;
      color: #fff;
      font-weight: 800;
      font-size: 16px;
      cursor: pointer;
    }
</style>