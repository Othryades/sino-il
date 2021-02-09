<template>
  <div class="intro-wrap">
    <div class="container py-5">    
        <div class="row">
            <div class="col-12 py-3 pb-4 text-center">
                <h1>2021 Governmental grants - Hangzhou</h1>
                <h2>Gongshu district</h2>
            </div>
            <div class="col-6">
                <p>
                    Hangzhou, China, is the capital of Zhejiang province. It sits at the head of Hangzhou Bay, which separates Shanghai and Ningbo. Marco Polo called it, 
                    "the most beautiful and splendid city in the world."<br/>                     
                    As the headquarters of Internet industry enterprises such as Alibaba, Hangzhou has also strongly attracted people who work in the Internet industry.  The city has developed many new industries, including medicine, information technology, 
                    heavy equipment, automotive components, household electrical appliances, electronics, telecommunication, fine chemicals, chemical fibre and food processing.
                </p>
            </div>
            <div class="col-6">
                <VueSlickCarousel v-bind="settings">
                <img class="" src="~assets/images/hangzhou.jpg" alt="bg" title="slider_1" loading="lazy"/>
                <img class="" src="~assets/images/hangzhou.jpg" alt="bg" title="slider_1" loading="lazy"/>
                </VueSlickCarousel>
            </div>            
        </div>
        <div class="row d-flex justify-content-center py-4">
            <div class="col-10">
                <div class="embed-responsive embed-responsive-16by9" preload="none">
                    <!-- <iframe class="embed-responsive-item" src="https://www.youtube.com/watch?v=watch?v=pc27fivPszM" allowfullscreen></iframe> -->
                    <iframe width="1280" height="720" src="https://www.youtube.com/embed/pc27fivPszM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
 
  export default {
    name: 'MyComponent',
    components: { VueSlickCarousel },
    data() {
      return {
        settings: {
          autoplay: true,
          dots: true,
        },
      }
    },
  }

</script> 
<style scoped>
    img{
        height: 300px;
        width: 100%;
        object-fit: cover;
        object-position: 0% 40%;
    }
    .intro-wrap{
        background-color: #fafafa;
    }
</style>