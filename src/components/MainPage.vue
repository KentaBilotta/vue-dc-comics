<template>
  <main>
    <div class="jumbo"></div>
    <div class="container">
      <div class="current">current series</div>
      <div class="cards">
        <CardPage
          v-for="objSeries in arrSeries"
          :key="objSeries.series"
          :imgUrl="objSeries.thumb"
          :titolo="objSeries.series"
        />
      </div>
      <div class="load-button">load more</div>
    </div>
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
import digitalImg from '@/img/buy-comics-digital-comics.png';
import merchandiseImg from '@/img/buy-comics-merchandise.png';
import subImg from '@/img/buy-comics-subscriptions.png';
import shopImg from '@/img/buy-comics-shop-locator.png';
import visaImg from '@/img/buy-dc-power-visa.svg';

import CardPage from '@/components/CardPage.vue';

export default {
  name: 'MainPage',
  components: {
    CardPage,
  },
  data() {
    return {
      buyComicsArray: [
        {
          img: digitalImg,
          text: 'digital comics',
        },
        {
          img: merchandiseImg,
          text: 'dc merchandise',
        },
        {
          img: subImg,
          text: 'subscription',
        },
        {
          img: shopImg,
          text: 'comic shop locator',
        },
        {
          img: visaImg,
          text: 'dc power visa',
        },
      ],
      arrSeries: [
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
          price: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
          price: '$2.99',
          series: 'Batgirl',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$3.99',
          series: 'Batman',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
          price: '$3.99',
          series: 'Batman/Superman',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
          price: '$4.99',
          series: 'Batman/Superman Annual',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
          price: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
          price: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
          price: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book',
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
          price: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel',
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
    .container{
      background-color: #1c1c1c;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 5rem;
      position: relative;

      .current{
        text-transform: uppercase;
        background-color: $main-blue;
        padding: 15px;
        position: absolute;
        top: 0;
        left: 10%;
        transform: translate(0, -50%);
      }
      .cards{
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      }

      .load-button{
          text-transform: uppercase;
          background-color: $main-blue;
          padding: 10px;
          width: 150px;
          text-align: center;
          border: 1px solid white;
          cursor: pointer;
          margin-top: 2rem;

          &:hover{
            background-color: white;
            color: $main-blue;
            border: 1px solid black;
          }
      }
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
          width: 80px;
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
