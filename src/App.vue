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
              <h1 class="save-the-date__title">Save the Date</h1>
              <h2 class="save-the-date__subtitle"><time datetime="2019-06-14T18:00:00.000Z">2019. június 14.</time></h2>
            </a>
          </section>
        </div>
      </div>
    </div>

    <nav class="main-navbar navbar sticky-top navbar-light navbar-expand-lg">
      <div class="container">
        <button @click="toggleNavigation" class="navbar-toggler ml-auto collapsed" type="button">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="main-nav">
          <div class="navbar-nav mx-auto">
            <a class="nav-item nav-link" v-for="({id, label}, idx) in sections"
              :key="id"
              :class="{'active': activeSectionIndex === idx}"
              :href="`#${id}`">{{label}}</a>
          </div>
      </div>
      </div>
    </nav>

    <section class="section section--first">
      <h1 class="sr-only">Zsuzska &amp; Laci</h1>
      <div class="container">
        <div class="bg-light">
          <article class="row align-items-center">
            <div class="col-sm-6 text-center">
              <div class="p-4">
                <img class="img-resp" src="./assets/images/zsuzska.jpg" alt="">
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
            <div class="col-sm-6 order-sm-2 text-center">
              <div class="p-4">
                <img class="img-resp" src="./assets/images/laci.jpg" alt="">
              </div>
            </div>
            <div class="col-sm-6 text-sm-right">
              <div class="p-4">
                <h1 class="section__block-title">A Vőlegény</h1>
                <p class="text-general">Zsuzskával való első találkozásom olyan volt, mint egy villámcsapás. Rögtön azt éreztem, igen ez a lány kell nekem! Ragyogó mosolyába azóta is mindennap beleszeretek. Zsuzska az a nő, akire igazán büszke lehetek, maximalizmusa számomra is motivációt jelent, hogy mindig odafigyelő és szerető férje legyek. Nagy öröm számomra, hogy mind a családja, mind a barátai szeretettel fogadtak. Azt szeretném, hogy szerelmünk stabil alapja legyen egy olyan családnak, amelyben a szeretet mindenkit körülvesz.</p>
                <h2 class="h4 cursive">- Laci</h2>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="when" class="section section--counter">
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

    <section id="where" class="section bg-light">
      <div class="container">
        <section-title>Helyszín</section-title>
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
                <h1 class="section__block-title text-primary">Egyházi ceremónia</h1>
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
                <h1 class="section__block-title text-primary">Vacsora &amp; Party</h1>
                <h2 class="h5">Diófa Étterem és Rendezvényház, 1171 Budapest, Szabadság sgrt. 1.</h2>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="about" class="section bg-gray">
      <div class="container">
        <section-title>Történetünk</section-title>

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
                <img src="./assets/images/01_itsamatch.jpg" class="img-resp" alt="">
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
                <img src="./assets/images/02_elsorandi.jpg" class="img-resp" alt="">
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
                <img src="./assets/images/03_nyaralas.jpg" class="img-resp" alt="">
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
                <img src="./assets/images/04_osszekoltozes.jpg" class="img-resp" alt="">
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
                <img src="./assets/images/05_eljegyzes.jpg" class="img-resp" alt="">
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
                <img src="./assets/images/06_esmost.jpg" class="img-resp" alt="">
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="contact" class="section bg-primary">
      <div class="container">
        <section-title title-class="section__title--light">Elérhetőségek</section-title>
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

    <section id="rsvp" class="section">
      <div class="container">
        <section-title>Tarts velünk!</section-title>
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
import RsvpForm from '@/components/RsvpForm'
import SectionTitle from '@/components/Title'

const theDate = new Date('2019-06-14T18:00:00.000Z')
const timeDiff = theDate.getTime() - Date.now()
export default {
  name: 'app',
  data () {
    return {
      interval: null,
      notifications: [],
      diff: Math.trunc(timeDiff / 1000),
      navbarClass: '',
      activeSectionIndex: -1,
      sections: [
        { id: 'when', label: 'Mikor' },
        { id: 'where', label: 'Helyszín' },
        { id: 'about', label: 'Történetünk' },
        { id: 'contact', label: 'Elérhetőségek' },
        { id: 'rsvp', label: 'Visszajelzés' }
      ]
    }
  },
  mounted () {
    this.interval = setInterval(() => {
      this.diff -= 1
    }, 1000)

    const navigationCallback = entries => {
      // entries.forEach(entry => {
      //   console.log(entry.target.id, entry.intersectionRatio * (entry.rootBounds.height / entry.boundingClientRect.height))
      //   const sectionIndex = this.sections.findIndex(({ id }) => entry.target.id === id)
      //   if (entry.intersectionRatio > 0.3) {
      //     this.activeSectionIndex = sectionIndex
      //   }
      // })
    }
    const navigationObserver = new IntersectionObserver(navigationCallback, {
      root: null,
      rootMargin: '0px',
      threshold: Array(100 + 1)
        .fill(0)
        .map((_, index) => index / 100 || 0)
    })
    this.sections.forEach(section => {
      navigationObserver.observe(document.getElementById(section.id))
    })
  },
  methods: {
    toggleNavigation () {
      document.getElementById('main-nav')
        .classList.toggle('collapse')
    }
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
    RsvpForm,
    SectionTitle
  }
}
</script>

<style lang="scss">
  @import './assets/styles/app';
  $navbar-height: 4rem;

  html {
    scroll-behavior: smooth;
  }

  .img-resp {
    max-height: 400px;
    max-width: 100%;
  }

  .main-navbar {
    background: #fff;
    margin-top: -$navbar-height;
    border-bottom: 1px solid $gray;

    .nav-link {
      font-size: 1.25rem;
      font-weight: 600;
      text-transform: uppercase;
      color: $body-color;

      &:hover {
        color: $primary;
      }
      &.active {
        color: $primary;
      }
    }

    .navbar-toggler {
      background-color: $primary;
    }
    .navbar-toggler-icon {
       background: str-replace(url("data:image/svg+xml,%3csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3e%3cpath stroke='#fff' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e"), "#", "%23");
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

  .section__block-title {
    font-size: 1.375rem;
    font-weight: 600;
    text-transform: uppercase;
  }

  .section--hero {
    height: 100vh;
    overflow: hidden;
    padding-bottom: $navbar-height;
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
    bottom: 150px;
    @include media-breakpoint-up(sm) {
      bottom: 200px;
    }
  }
  .hero__title {
    font-family: $font-family-cursive;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.6);
    font-size: 2.825rem;
    @include media-breakpoint-up(sm) {
      font-size: 5rem;
    }
    margin-top: 3rem;
  }
  .hero__subtitle {
    font-size: 1.75rem;
    @include media-breakpoint-up(sm) {
      font-size: 2.25rem;
    }
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
    height: 130px;
    @include media-breakpoint-up(sm) {
      height: 140px;
    }
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

    width: 220px;
    height: 220px;
    @include media-breakpoint-up(sm) {
      width: 280px;
      height: 280px;
    }
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
    font-size: 2rem;
    margin-bottom: 0;
    @include media-breakpoint-up(sm) {
      font-size: 2.5rem;
    }
  }
  .save-the-date__subtitle {
    font-size: 1.75rem;
    @include media-breakpoint-up(sm) {
      font-size: 2.5rem;
    }
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
