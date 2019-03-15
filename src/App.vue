<template>
  <div id="app">
    <div class="section--hero bg-primary text-white">
      <div class="container">
        <div class="d-flex flex-column justify-content-center align-items-center h-100">
          <div class="hero__text">
            <h1 class="hero__title">Zsuzska &amp; Laci</h1>
            <h2 class="hero__subtitle">Összeházasodnak</h2>
          </div>
          <section class="hero__footer text-center mt-auto">
            <a target="_blank" class="save-the-date text-white" href="https://calendar.google.com/event?action=TEMPLATE&amp;tmeid=N2c2MWo5Mjc4YjA2b3ZjZDhocGdmbnAwaHIgZmVyZW5jLnN0aWN6YUBt&amp;tmsrc=ferenc.sticza%40gmail.com">
              <h1 class="save-the-date__title">Jegyezd fel!</h1>
              <h2><time datetime="2019-06-14T18:00:00.000Z">2019. június 14.</time></h2>
            </a>
          </section>
        </div>
      </div>

      <nav class="main-navbar navbar sticky-top navbar-expand-lg">
        <div class="container">
          <button class="navbar-toggler" type="button">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="main-nav">
            <div class="navbar-nav mx-auto">
                <a class="nav-item nav-link" href="#when">Mikor</a>
                <a class="nav-item nav-link" href="#where">Helyszín</a>
                <a class="nav-item nav-link" href="#about-us">Történetünk</a>
                <a class="nav-item nav-link" href="#contact">Elérhetőségek</a>
                <a class="nav-item nav-link" href="#rsvp">RSVP</a>
            </div>
        </div>
        </div>
      </nav>

    </div>

    <section class="section section--first">
      <h1 class="sr-only">Zsuzska &amp; Laci</h1>
      <div class="container">
        <div class="bg-light">
          <article class="row align-items-center">
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img src="./assets/images/zsuzska.jpg" height="400" alt="">
              </div>
            </div>
            <div class="col-sm-6">
              <div class="p-4">
                <h1 class="section__block-title">A Menyasszony</h1>
                <p class="text-general">Amikor Laci betoppant az életemben, vele együtt beköszöntött a szerelem is. újra elkezdtem látni a színeket, élvezni a mindennapokat és rengeteget mosolyogtam neki köszönhetően. Mindig megnevettet. Büszkén mutattam be barátaimnak és családomnak a férfit, aki mellett boldog vagyok. Most pedig hihetetlenül izgatott vagyok az esküvőnk végett. Hálás vagyok, hogy rátaláltam arra az emberre, akivel le szeretném élni az egész életemet. Laci jelenti számomra a biztonságot, a szerelmet és a társat egy életen át.</p>
                <h2 class="h4 font-bold cursive">- Zsuzska</h2>
              </div>
            </div>
          </article>
          <article class="row align-items-center">
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title">A Vőlegény</h1>
                <p class="text-general">Zsuzskával való első találkozásom olyan volt, mint egy villámcsapás. Rögtön azt éreztem, igen ez a lány kell nekem! Ragyogó mosolyába azóta is mindennap beleszeretek. Zsuzska az a nő, akire igazán büszke lehetek, maximalizmusa számomra is motivációt jelent, hogy mindig odafigyelő és szerető férje legyek. Nagy öröm számomra, hogy mind a családja, mind a barátai szeretettel fogadtak. Azt szeretném, hogy szerelmünk stabil alapja legyen egy olyan családnak, amelyben a szeretet mindenkit körülvesz.</p>
                <h2 class="h4 cursive">- Laci</h2>
              </div>
            </div>
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img src="./assets/images/laci.jpg" height="400" alt="">
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section section--counter">
      <div class="container">
        <h1 class="sr-only">Mikor</h1>
        <div class="row align-item-center">
          <div class="col-md-4 align-self-center">
            <h2 class="cursive text-white text-shadow">
              <div class="h2">
                Már alig várjuk...
              </div>
              <div class="h1">
                A nagy kalandot
              </div>
            </h2>
          </div>
          <div class="col-md-8">
            <div class="row">
              <div class="col-sm-6 col-md-3">
                <div class="counter-box">
                  <div class="counter">{{ days | leftPad }}</div>
                  <div class="counter-unit">Nap</div>
                </div>
              </div>
              <div class="col-sm-6 col-md-3">
                <div class="counter-box">
                  <div class="counter">{{ hours | leftPad }}</div>
                  <div class="counter-unit">Óra</div>
                </div>
              </div>
              <div class="col-sm-6 col-md-3">
                <div class="counter-box">
                  <div class="counter">{{ minutes | leftPad }}</div>
                  <div class="counter-unit">Perc</div>
                </div>
              </div>
              <div class="col-sm-6 col-md-3">
                <div class="counter-box">
                  <div class="counter">{{ seconds | leftPad }}</div>
                  <div class="counter-unit">Mp</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section bg-light">
      <div class="container">
        <div class="text-center">
          <h1 class="section__title">Helyszín</h1>
        </div>
        <div class="bg-white">

          <article class="row align-items-center">
            <div class="col-sm-6">
              <div class="p-4">
                <div class="embed-responsive embed-responsive-21by9">
                  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2690.332608903897!2d19.345927415840144!3d47.6002218964115!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4741c92524031581%3A0xa5005dbd674811e!2sReformed+Church!5e0!3m2!1sen!2shu!4v1552681698347"
                    class="embed-responsive-item"
                    width="700" height="300" frameborder="0" style="border:0" allowfullscreen></iframe>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="p-4">
                <h1 class="section__block-title">Egyházi ceremónia</h1>
                <h2 class="h5">Evangélikus templom, 2100 Gödöllő, Petőfi tér</h2>
              </div>
            </div>
          </article>
          <article class="row align-items-center">
            <div class="col-sm-6 order-sm-2">
              <div class="p-4">
                <div class="embed-responsive embed-responsive-21by9">
                  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2696.1664145203063!2d19.26891041598991!3d47.486671379176734!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4741c6b15e1656bf%3A0x110bc820d4b2eab7!2zRGnDs2ZhIMOJdHRlcmVtIMOpcyBSZW5kZXp2w6lueWjDoXo!5e0!3m2!1sen!2shu!4v1551993824839"
                    class="embed-responsive-item"
                    width="700" height="300" frameborder="0" style="border:0" allowfullscreen></iframe>
                </div>
              </div>
            </div>
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title">Vacsora &amp; Party</h1>
                <h2 class="h5">Diófa Étterem és Rendezvényház, 1171 Budapest, Szabadság sgrt. 1.</h2>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section bg-gray">
      <div class="container">
        <div class="text-center">
          <h1 class="section__title">Történetünk</h1>
        </div>

        <div class="bg-light">
          <article class="row align-items-center">
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title text-primary">It’s a Match!</h1>
                <time class="font-bold" datatime="2016-07-31">2016.07.31.</time>
                <p class="text-general">Itt kezdődött minden! Egy társkereső applikáción keresztül ismerkedett meg Zsuzska és Laci. A néhány napon át tartó intenzív üzenetváltást követően mindkettejükben egyre nagyobb volt a kíváncsiság a másik iránt.</p>
              </div>
            </div>
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-1.jpg" height="400" alt="">
              </div>
            </div>
          </article>

          <article class="row align-items-center">
            <div class="col-sm-6 order-sm-2">
              <div class="p-4">
                <h1 class="section__block-title text-primary">Első randi</h1>
                <time class="font-bold" datatime="2016-08-06">2016.08.06.</time>
                <p class="text-general">Szombat este Zsuzska kedvenc terén, a Széll Kálmán téren találkoztak. Egy romantikus séta során ismerték meg egymást végre személyesen. Már akkor és ott tudták mindketten, hogy az az este valaminek a kezdete volt. </p>
              </div>
            </div>
            <div class="col-sm-6 order-sm-1 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-2.jpg" height="400" alt="">
              </div>
            </div>
          </article>

          <article class="row align-items-center">
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title text-primary">Első közös nyaralás</h1>
                <time class="font-bold" datatime="2017-01-29">2017.01.29</time>
                <p class="text-general">Egy álom vált valóra azzal, amikor elutaztak a napsütötte Barcelonába. A tengerparton sétálva Laci felvetette az összeköltözés gondolatát. Szándékát megerősítve meglepte Zsuzskát egy helyben készített kulcstartóval. Az utazás azóta közös hobbijukká vált.</p>
              </div>
            </div>
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-3.jpg" height="400" alt="">
              </div>
            </div>
          </article>

          <article class="row align-items-center">
            <div class="col-sm-6 order-sm-2">
              <div class="p-4">
                <h1 class="section__block-title text-primary">Összeköltözés</h1>
                <time class="font-bold" datatime="2017-02-25">2017.02.25.</time>
                <p class="text-general">Fontos mérföldkő volt ez az életükben. A doboz hegyek mögött mindketten látták a boldog jövőt. Zsuzska beköltözésével vált a lakás igazi otthonná.</p>
              </div>
            </div>
            <div class="col-sm-6 order-sm-1 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-4.jpg" height="400" alt="">
              </div>
            </div>
          </article>

          <article class="row align-items-center">
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title text-primary">Eljegyzés</h1>
                <time class="font-bold" datatime="2018-02-06">2018.02.06.</time>
                <p class="text-general">Rómából érkeztek haza azon a napon. Romantikus vacsorával ünnepelték meg az első találkozásuk óta eltel másfél évet, amikor is Laci feltette azt a bizonyos kérdést Zsuzska számára. A meglepettség utáni zokogást követően jött a válasz: Igen!</p>
              </div>
            </div>
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-5.jpg" height="400" alt="">
              </div>
            </div>
          </article>

          <article class="row align-items-center">
            <div class="col-sm-6 order-sm-2">
              <div class="p-4">
                <h1 class="section__block-title text-primary">És most...</h1>
                <time class="font-bold" datatime="2019-06-14">2019.06.14.</time>
                <p class="text-general">...készen állnak arra, hogy családjuk és barátaik jelenlétében örök hűséget fogadjanak egymásnak.</p>
              </div>
            </div>
            <div class="col-sm-6 order-sm-1 text-center">
              <div class="p-4">
                <img src="./assets/images/laci-zsuzska-6.jpg" height="400" alt="">
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section class="section bg-primary">
      <div class="container">
        <div class="text-center">
          <h1 class="section__title section__title--light">Elérhetőségek</h1>
        </div>
        <div class="row text-center">
          <article class="col-sm-6">
            <h1 class="section__block-title mt-3">Menyasszony - Zsuzska</h1>
            <a class="h3 text-white" href="tel:+36309435814">+36 30 943 5814</a>
          </article>
          <article class="col-sm-6">
            <h1 class="section__block-title mt-3">Vőlegény - Laci</h1>
            <a class="h3 text-white" href="tel:+36706327662">+36 70 632 7662</a>
          </article>
        </div>
        <div class="row text-center">
          <article class="col-sm-4">
            <h1 class="section__block-title mt-4">Taxi - Lajos</h1>
            <a class="h3 text-white" href="tel:+36309664961">+36 30 966 4961</a>
          </article>
          <article class="col-sm-4">
            <h1 class="section__block-title mt-4">Ceremóniamester - Gémesi Gergő</h1>
            <a class="h3 text-white" href="tel:+36303931268">+36 30 393 1268</a>
          </article>
          <article class="col-sm-4">
            <h1 class="section__block-title mt-4">Taxi - Tomi</h1>
            <a class="h3 text-white" href="tel:+36202870653">+36 20 287 0653</a>
          </article>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="text-center">
          <h1 class="section__title">Tarts velünk!</h1>
        </div>
        <div class="row">
          <div class="col-sm-8 offset-sm-2">
            <h2 class="section__block-title">Küldd el a visszajelzésed mielőbb!</h2>
            <rsvp-form />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// import Alert from '@/components/Alert'
import RsvpForm from '@/components/RsvpForm'

const theDate = new Date('2019-06-14T18:00:00.000Z')
const timeDiff = theDate.getTime() - Date.now()
export default {
  name: 'app',
  data () {
    return {
      interval: null,
      notifications: [],
      diff: Math.trunc(timeDiff / 1000)
    }
  },
  created () {
    this.interval = setInterval(() => {
      this.diff -= 1
    }, 1000)
  },
  computed: {
    seconds () {
      return Math.trunc(this.diff) % 60
    },
    minutes () {
      return Math.trunc(this.diff / 60) % 60
    },
    hours () {
      return Math.trunc(this.diff / 60 / 60) % 24
    },
    days () {
      return Math.trunc(this.diff / 60 / 60 / 24)
    }
  },
  filters: {
    leftPad (value) {
      if (value.toString().length <= 1) {
        return '0' + value.toString()
      }
      return value.toString()
    }
  },
  destroyed () {
    clearInterval(this.interval)
  },
  components: {
    // Alert,
    RsvpForm
  }
}
</script>

<style lang="scss">
  @import './assets/styles/app';
  .main-navbar {
    background: #fff;
    border-bottom: 1px solid $gray;

    .nav-link {
      font-size: 1.25rem;
      font-weight: 600;
      text-transform: uppercase;
      color: $body-color;

      &:hover {
        color: $primary;
      }
    }
  }

  .section {
    padding-top: 5rem;
    padding-bottom: 5rem;
  }
  .section--first {
    margin-top: 2px;
    border-top: 1px solid $gray;
  }

  .section__title {
    display: inline-block;
    background-color: transparentize($primary, 0.9);
    color: #848383;
    padding: 1rem 2rem 0.5rem;
    margin-bottom: 3rem;
    font-family: $font-family-cursive;
    font-size: 2.5rem;
    line-height: 2.5rem;
    border-top: 2px solid transparentize($primary, 0.9);
    border-bottom: 2px solid transparentize($primary, 0.9);
  }

  .section__title--light {
    background-color: transparentize(#fff, 0.9);
    color: #fff;
    border-top: 2px solid transparentize(#fff, 0.9);
    border-bottom: 2px solid transparentize(#fff, 0.9);
  }

  .section__block-title {
    font-size: 1.375rem;
    font-weight: 600;
    text-transform: uppercase;
  }

  .section--hero {
    height: 100vh;
    overflow: hidden;
    padding-bottom: 4.425rem;
    background-image: url('./assets/images/header-photo.jpg');
    background-position: 50% 0;
    background-size: cover;
    position: relative;
    z-index: 0;
    &:before {
      content: "";
      position: absolute;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      background: rgba(0, 0, 0, 0.2);
    }

    .container {
      position: relative;
      z-index: 2;
      height: 100%;
    }
  }
  .hero__text {
    text-align: center;
    position: absolute;
    bottom: 200px;
  }
  .hero__title {
    font-family: $font-family-cursive;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
    font-size: 5rem;
    margin-top: 3rem;
  }
  .hero__subtitle {
    font-size: 2.25rem;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
    letter-spacing: .1em;
    text-transform: uppercase;
    margin-top: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    border-top: 1px solid #fff;
    border-bottom: 1px solid #fff;
  }

  .hero__footer {
    height: 140px;
  }

  .text-general {
    font-size: 1.175rem;
    line-height: 1.5;
  }

  .save-the-date {
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
    background-color: $primary;
    position: relative;
    @include border-radius(50%);
    transition: 1s 2.3s ease-in-out;
    display: block;
    width: 280px;
    height: 280px;
    &:hover {
      text-decoration: none;
    }

    &::before {
      content: "";
      position: absolute;
      @include border-radius(50%);
      z-index: -1;
      background-color: transparentize($primary, 0.7);
      width: 110%;
      height: 110%;
      left: -5%;
      top: -5%;
      animation: save-the-date-pulse 1s infinite;
    }

    @keyframes save-the-date-pulse {
      from {
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
      }

      50% {
        -webkit-transform: scale3d(0.95, 0.95, 0.95);
        transform: scale3d(0.95, 0.95, 0.95);
      }

      to {
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
      }
    }
  }

  .save-the-date__title {
    font-family: $font-family-cursive;
    padding-top: 2.5rem;
  }

  .section--counter {
    background-image: url('./assets/images/countdown-bg.jpg');
    background-position: 50% 50%;
    background-size: cover;
    position: relative;
    z-index: 0;
    &:before {
      content: "";
      position: absolute;
      top: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      background: rgba(0, 0, 0, 0.2);
    }
    .container {
      position: relative;
      z-index: 2;
      height: 100%;
    }
  }

  .counter-box {
    background: rgba(255, 255, 255, 0.9);
    text-align: center;
    padding: 15px;
    border-radius: 5px;
    border: 5px solid rgba(0, 0, 0, 0.1);
    color: $primary;

    .counter {
      font-size: 2rem;
      font-weight: 700;
    }
    .counter-unit {
      font-size: 0.775rem;
      text-transform: uppercase;

    }
  }

  .cursive {
    font-family: $font-family-cursive;
  }
  .text-shadow {
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
  }

</style>
