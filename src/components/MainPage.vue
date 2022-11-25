<template>
  <main>
    <div class="jumbo"></div>
    <div class="content"> --> Content Goes Here</div>
    <nav>
      <div v-for="element in buyComicsArray" :key="element.text">
        <img :src="element.img" alt="icon">
        <div>{{ element.text }}</div>
      </div>
    </nav>
    <section>
      <div class="link-list">
        <div class="item">
          <div class="item-name">dc comics</div>
            <a href="#!">characters</a>
            <a href="#!">comics</a>
            <a href="#!">movies</a>
            <a href="#!">TV</a>
            <a href="#!">games</a>
            <a href="#!">videos</a>
            <a href="#!">news</a>
        </div>
        <div class="item">
          <div class="item-name">shop</div>
            <a href="#!">shop dc</a>
            <a href="#!">shop dc collection</a>
        </div>
        <div class="item">
          <div class="item-name">dc</div>
            <a href="#!">terms of use</a>
            <a href="#!">privacy policy (new)</a>
            <a href="#!">ad choises</a>
            <a href="#!">advertising</a>
            <a href="#!">jobs</a>
            <a href="#!">subscriptions</a>
            <a href="#!">talent workshops</a>
            <a href="#!">CPSC certificates</a>
            <a href="#!">ratings</a>
            <a href="#!">shop help</a>
            <a href="#!">contact us</a>
        </div>
        <div class="item">
          <div class="item-name">sites</div>
            <a href="#!">DC</a>
            <a href="#!">MAD magazine</a>
            <a href="#!">DC kids</a>
            <a href="#!">DC universe</a>
            <a href="#!">DC power visa</a>
        </div>
      </div>
      <div class="bg-logo"></div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'MainPage',
  data() {
    return {
      buyComicsArray: [
        {
          img: '@/img/buy-comics-digital-comics.png',
          text: 'digital comics',
        },
        {
          img: '@/img/buy-comics-merchandise.png',
          text: 'dc merchandise',
        },
        {
          img: '@/img/buy-comics-subscriptions.png',
          text: 'subscription',
        },
        {
          img: '@/img/buy-comics-shop-locator.png',
          text: 'comic shop locator',
        },
        {
          img: '@/img/buy-dc-power-visa.svg',
          text: 'dc power visa',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
  $main-blue: #0282f9;

  main{
    color: white;

    .jumbo{
      height: 40vh;
      background-image: url("../img/jumbotron.jpg");
      background-size: cover;
      background-position: top center;
    }
    .content{
      background-color: black;
      font-size: 2rem;
      padding: 2rem;
    }

    h1{
      background-color: black;
      padding: 1.5rem;
    }
    nav{
      background-color: $main-blue;
      display: flex;
      justify-content: space-around;
      padding: 1rem;
      div{
        text-transform: uppercase;
        display: flex;
        align-items: center;
        img{
          width: 50px;
          padding: 1rem;
        }
      }
    }
    section{
      height: 40vh;
      background-image: url("../img/footer-bg.jpg");
      display: flex;
      justify-content: space-around;

      .link-list{
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
      }

      .item{
        display: flex;
        flex-direction: column;
        padding: .5rem;
      }

      .item .item-name{
        text-transform: uppercase;
        font-weight: bold;
        padding: 5px;
      }

      .item a{
        text-decoration: none;
        color: grey;
        text-transform: capitalize;
        font-size: 0.9rem;
        font-weight: lighter;
        padding: 3px;
        &:hover{
          text-decoration: underline;
        }
      }
      .bg-logo{
        width: 400px;
        height: 100%;
        background-image: url("../img/dc-logo-bg.png");
        background-size: 100%;
        background-position: center;
        background-repeat: no-repeat;
      }
    }

  }

</style>
