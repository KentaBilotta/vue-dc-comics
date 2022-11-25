<template>
  <div class="card">
    <img :src="imgUrl" alt="">
    <div class="title">{{ titolo }}</div>
  </div>
</template>

<script>
export default {
  name: 'CardPage',
  props: {
    imgUrl: String,
    titolo: String,
  },
};
</script>

<style lang="scss" scoped>
.card{
  color: white;
  text-transform: uppercase;
  width: calc(100% / 8);
  margin: 15px;

  img{
    width: 100%;
    height: 200px;;
    object-fit: cover;
    object-position: top center;
  }

  .title{
    font-weight: lighter;
    margin-top: 20px;
  }
}

</style>
