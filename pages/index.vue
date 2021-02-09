<template>
  <section class="home">
    <div class="container-fluid hero">
      <div class="container hero">
        <div class="hero__image"></div>

        <div class="hero__text container--pall">
          <h1>Sino-israel cross border consulting</h1>
          <p>
            <strong>Our mission:</strong> to brige the distance between china
            and israel, bring business to both sides, help israelis going to
            chinese market
          </p>
          <p>
            Our vision: make china another habita for israeli startups to grow
          </p>
          <a href="#" class="button hero__cta">Request Invite</a>
        </div>
      </div>
    </div>
    <section class="feature">
      <div class="feature__content container py-5">
        <div class="feature__intro">
          <h2>What we do</h2>
          <!-- <p>
            We leverage Open Banking to turn your bank account into your
            financial hub. Control your finances like never before.
          </p> -->
        </div>

        <div class="feature__grid">
          <div class="feature__item">
            <div class="feature__icon">
              <i class="fas fa-map-signs"></i>
            </div>
            <div class="feature__title">Startups localization</div>
            <div class="feature__description">                          
              We provide startups with comprehensive localization services including registration consultant, legal advice, accountant assistant etc.              
            </div>
          </div>

          <div class="feature__item">
            <div class="feature__icon">
              <i class="fas fa-funnel-dollar"></i>
            </div>
            <div class="feature__title">Investment/ Grants</div>
            <div class="feature__description">               
                We connect startups to investment opportunities and help them raising funds in china.              
            </div>
          </div>

          <div class="feature__item">
            <div class="feature__icon">
              <i class="fas fa-american-sign-language-interpreting"></i>
            </div>
            <div class="feature__title">Innovation community</div>
            <div class="feature__description">
                We organize hot events for Our startups community and We share industry information.
            </div>
          </div>

        </div>
      </div>
    </section>

    <div class="container our-work py-5">
      <h2 class="text-center">We focus, we look for tomorrow</h2>
      <div class="row pt-3">
        <div class="col-6 col-md-3 text-center">
          <i class="fas fa-robot"></i>
          <p class="mt-3 mb-2">人工智能</p>
          <p class="mb-2">AI</p>
        </div>
        <div class="col-6 col-md-3 text-center">
          <i class="fas fa-hand-holding-medical"></i>
          <p class="mt-3 mb-2">大健康</p>
          <p class="mb-2">Healthcare</p>
        </div>
        <div class="col-6 col-md-3 text-center">
          <i class="fas fa-car"></i>
          <p class="mt-3 mb-2">智能网联汽车</p>
          <p class="mb-2">ICV</p>
        </div>
        <div class="col-6 col-md-3 text-center">
          <i class="fas fa-plug"></i>
          <p class="mt-3 mb-2">新能源</p>
          <p class="mb-2">New energy</p>
        </div>
      </div>
    </div>

    <div class="our-team">
      <div class="article__content container container--pall">
        <h2>Our team</h2>

        <div class="article__grid">
          <div href="#" class="article__item">
            <div class="article__image"></div>
            <div class="article__text">
              <div class="article__author">Bella Wu</div>
              <div class="article__title">Founder</div>
              <div class="article__description">
                Can calmly deal with emergencies and problems on the programme,
                great pressure resistance. Affinity, Endurance, Social skills:
                feeling easy and flexible facing people of all ages and social
                classes.
              </div>
              <div class="mt-3">
                <a
                  href="https://www.linkedin.com/in/bella-wu-061146159/"
                  target="_blank"
                  ><i class="fab fa-linkedin"></i
                ></a>
              </div>
            </div>
          </div>

          <div href="#" class="article__item">
            <div class="article__image article__image_2"></div>

            <div class="article__text">
              <div class="article__author">Coco</div>
              <div class="article__title">Senior Consultant</div>
              <div class="article__description">
                Our simple budgeting feature allows you to separate out your
                spending and set realistic limits each month. That means you …
              </div>
              <div class="mt-3">
                <a href="https://www.linkedin.com/in/bella-wu-061146159/">
                  <i class="fab fa-linkedin"></i>
                </a>
              </div>
            </div>
          </div>

          <div href="#" class="article__item">
            <div class="article__image article__image_3"></div>
            <div class="article__text">
              <div class="article__author">Moris Iarossi</div>
              <div class="article__title">Consultant</div>
              <div class="article__description">
                We want you to enjoy your travels. This is why we don’t charge
                any fees on purchases while you’re abroad. We’ll even show you …
              </div>
              <div class="mt-3">
                <a href="https://www.linkedin.com/in/bella-wu-061146159/"
                  ><i class="fab fa-linkedin"></i
                ></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row my-3">
        <div class="col-12">
          <div id="map-wrap" style="height: 50vh">
            <client-only>
              <l-map
                :zoom="3"
                :center="[30.129471793805592, 78.79503578552495]"
              >
                <l-tile-layer
                  url="http://{s}.tile.osm.org/{z}/{x}/{y}.png"
                ></l-tile-layer>
                <l-marker :lat-lng="[30.319602421767325, 120.1449368898419]"
                  ><l-tooltip>Our office in Hangzhou</l-tooltip></l-marker
                >
                <l-marker :lat-lng="[32.08279121881395, 34.77430460829394]"
                  ><l-tooltip>Our office in Tel Aviv</l-tooltip></l-marker
                >
                <l-marker :lat-lng="[31.246778246432836, 121.46440018662439]"
                  ><l-tooltip>Our local partner</l-tooltip></l-marker
                >
                <l-marker :lat-lng="[24.51403728430072, 118.15117190563794]"
                  ><l-tooltip>Our local partner</l-tooltip></l-marker
                >
              </l-map>
            </client-only>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.hero {
  background-color: #fafafa;
}

@media (min-width: 64em) {
  .hero.container {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
  }
}

.hero__image {
  position: relative;
  /* background-image: url("/images/bg-intro-mobile.svg"); */
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  min-height: 10.5rem;
}

@media (min-width: 40em) {
  .hero__image {
    min-height: 20.5rem;
  }
}

@media (min-width: 64em) {
  .hero__image {
    -webkit-box-flex: 3;
    -ms-flex: 3;
    flex: 3;
    -webkit-box-ordinal-group: 3;
    -ms-flex-order: 2;
    order: 2;
    /* height: 41rem; */
    background-image: none;
  }
}

@media (min-width: 64em) {
}

.hero__image::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: url("~assets/images/ddd.jpg");
  background-size: 100%;
  background-repeat: no-repeat;
  background-position: center bottom;
}

@media (min-width: 40em) {
  .hero__image::after {
    /* background-size: 52%; */
  }
}

@media (min-width: 64em) {
  .hero__image::after {
    width: 120%;
    /* height: 122%;
    background-size: 94%;
    background-position: center 150%; */
    left: 25%;
    /* top: -10%; */
  }
}

.hero__text {
  text-align: center;
}

@media (min-width: 64em) {
  .hero__text {
    -webkit-box-flex: 3;
    -ms-flex: 3;
    flex: 3;
    -webkit-box-ordinal-group: 2;
    -ms-flex-order: 1;
    order: 1;
    text-align: left;
  }
}


.feature {
  background-color: #f3f4f6;
  text-align: center;
}

@media (min-width: 40em) {
  .feature {
    text-align: left;
  }
}

.feature__intro {
  margin-bottom: 3.75rem;
}
.feature__intro h2{
  text-align: center;
}
.feature__item .feature__icon{
  color: #2d314d;
}

@media (min-width: 40em) {
  .feature__grid {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
        flex-wrap: wrap;
  }
}

.feature__item {
  padding: 0.9375rem;
}

@media (min-width: 40em) {
  .feature__item {
    -webkit-box-flex: 0;
        -ms-flex: 0 0 50%;
            flex: 0 0 50%;
  }
}

@media (min-width: 64em) {
  .feature__item {
    -webkit-box-flex: 1;
        -ms-flex: 1;
            flex: 1;
  }
}

.feature__icon {
  margin-bottom: 1.875rem;
  text-align: center;
  font-size: 35px;
}

@media (min-width: 64em) {
  .feature__icon {
    margin-bottom: 2.75rem;
  }
}

.feature__title {
  font-size: 1.25rem;
  font-weight: 300;
  line-height: 1.15;
  color: #2d314d;
  margin-bottom: 1rem;
  text-align: center;
}

@media (min-width: 64em) {
  .feature__title {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
  }
}

.feature__description {
  font-size: 0.975rem;
  line-height: 1.5;
  text-align: center;
}




.our-team {
  background-color: #fafafa;
}
.articles {
  background-color: #fafafa;
}

.article__grid {
  display: -ms-grid;
  display: grid;
  -ms-grid-columns: 1fr;
  grid-template-columns: 1fr;
  gap: 1.875rem;
}

@media (min-width: 40em) {
  .article__grid {
    -ms-grid-columns: (1fr) [2];
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 64em) {
  .article__grid {
    -ms-grid-columns: (1fr) [4];
    grid-template-columns: repeat(4, 1fr);
  }
}

.article__item {
  border-radius: 0.3125rem;
  overflow: hidden;
  background-color: white;
  -webkit-box-shadow: 0px 3px 12px rgba(0, 0, 0, 0.15);
  box-shadow: 0px 3px 12px rgba(0, 0, 0, 0.15);
  -webkit-transition: all 150ms ease-in-out;
  transition: all 150ms ease-in-out;
}

.article__item:hover {
  -webkit-transform: scale(1.05);
  transform: scale(1.05);
}

.article__image {
  height: 12.5rem;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  background-image: url("~assets/images/bella_Copy.jpeg");
}
.article__image_2 {
  background-image: url("~assets/images/coco.png");
}
.article__image_3 {
  background-image: url("~assets/images/download.png");
  background-position: top;
}

.article__text {
  padding: 1.875rem 1.875rem 2.5rem 1.875rem;
  color: #9698a6;
}
.article__item i {
  color: #2d314d;
}

@media (min-width: 40em) {
  .article__text {
    padding: 1.875rem 1.5625rem;
  }
}

.article__author {
  font-size: 1.3rem;
  margin-bottom: 0.75rem;
}

.article__title {
  font-size: 1.0625rem;
  line-height: 1.2;
  color: #2d314d;
  margin-bottom: 0.5rem;
}

.article__description {
  font-size: 0.8125rem;
}
.our-work img {
  height: 100px;
}
.our-work i {
  font-size: 100px;
  color: #2d314d;
  opacity: 0.6;
}
.our-work i:hover {
  opacity: 1;
}
</style>
