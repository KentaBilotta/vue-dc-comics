<template>
  <div>
    <HeaderPage></HeaderPage>
    <MainPage></MainPage>
    <FooterPage></FooterPage>
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';
import FooterPage from '@/components/FooterPage.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
    FooterPage,
  },
};
</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html{
  font-family: "Roboto", Sans-serif;
}

</style>
