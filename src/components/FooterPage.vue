<template>
  <footer>
    <div class="sign-button">sing-up now!</div>
    <div class="socials">
      <div class="follow">follow us</div>
      <div class="icons">
        <img src="@/img/footer-facebook.png" alt="">
        <img src="@/img/footer-twitter.png" alt="">
        <img src="@/img/footer-youtube.png" alt="">
        <img src="@/img/footer-pinterest.png" alt="">
        <img src="@/img/footer-periscope.png" alt="">
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterPage',
};
</script>

<style lang="scss" scoped>
$footer-gray: #303030;
$main-blue: #0282f9;

footer{
  background-color: $footer-gray;
  height: 12vh;
  display: flex;
  justify-content: space-around;
  align-items: center;

  .sign-button{
    color: white;
    text-transform: uppercase;
    padding: .5rem;
    border: 2px solid $main-blue;
    width: fit-content;
    cursor: pointer;
  }

  .socials{
    display: flex;
  }
  .socials .follow{
    color: $main-blue;
    font-size: 1.2rem;
    font-weight: bold;
    text-transform: uppercase;
    padding: 1rem;
  }

  .icons img{
    width: 30px;
    margin: .5rem;
  }
}

</style>
