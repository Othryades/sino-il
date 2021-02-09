<template>
<div>
    <footer class="footer">
      <div class="container">
        <a class="footer__logo" href="#">
          <img src="~/assets/images/logo_footer.png" loading="lazy"/>
        </a>

        <div class="footer__social">
          <a href="#">
            <i class="fab fa-linkedin"></i>
          </a>
          <a href="#">
            <i class="fab fa-facebook"></i>
          </a>
        </div>

        <div class="footer__links col1">
          <nuxt-link to="/about-us" class="first__link">About Us</nuxt-link>
          <nuxt-link to="/contact" class="first__link">Contact</nuxt-link>
          <nuxt-link to="/careers" class="first__link">Careers</nuxt-link>
        </div>

        <div class="footer__links col2">
          <nuxt-link to="/privacy-policy" class="">Privacy Policy</nuxt-link>
        </div>

        <div class="footer__cta">
          <a href="#" class="button">Forecast 2021</a>
        </div>

        <div class="footer__copyright">
          &copy; sino-israel cross border consulting. All Rights Reserved.<br/>
          <!-- <i class="lni lni-map-marker"></i> Tel Aviv, Israel -  China -->

        </div>
      </div>
    </footer>
      <div class="attribution px-3">        
      Coded by <a href="#"><img src="~/assets/images/coder.gif" alt="coder" style="height:30px"></a>
      </div>
    </div>
</template>

<style>
/* footer */
.footer {
  background-color: #2d314d;
  color: white;
  padding: 2.5rem;
  text-align: center;
}

@media (min-width: 64em) {
  .footer .container {
    display: -ms-grid;
    display: grid;
    -ms-grid-columns: 2fr 1fr 1fr 3fr;
        grid-template-columns: 2fr 1fr 1fr 3fr;
    -ms-grid-rows: 1fr auto;
        grid-template-rows: 1fr auto;
        grid-template-areas: "logo links1 links2 cta"
 "social links1 links2 copyright";
    gap: 1rem;
    justify-items: start;
  }
}

.footer a {
  color: white;
}

.footer__logo {
  display: inline-block;
}

@media (max-width: 63.9375em) {
  .footer__logo {
    margin-bottom: 1.875rem;
  }
}

@media (min-width: 64em) {
  .footer__logo {
    grid-area: logo;
  }
}

@media (max-width: 63.9375em) {
  .footer__social {
    margin-bottom: 1.875rem;
  }
}

@media (min-width: 64em) {
  .footer__social {
    grid-area: social;
    -ms-flex-item-align: end;
        -ms-grid-row-align: end;
        align-self: end;
  }
}

.footer__social a {
  display: inline-block;
  height: 1.25rem;
}

.footer__social a {
  -webkit-transition: fill 150ms ease-in-out;
  transition: fill 150ms ease-in-out;
}

.footer__social a:hover {
  color: #31d35c;
}

.footer__social a:not(:last-child) {
  margin-right: 1rem;
}

.footer__links {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
      -ms-flex-direction: column;
          flex-direction: column;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  font-size: 0.9375rem;
}

@media (min-width: 64em) {
  .footer__links {
    -webkit-box-pack: justify;
        -ms-flex-pack: justify;
            justify-content: space-between;
    -webkit-box-align: start;
        -ms-flex-align: start;
            align-items: start;
  }
}

@media (min-width: 64em) {
  .footer__links.col1 {
    grid-area: links1;
  }
}

@media (max-width: 63.9375em) {
  .footer__links.col2 {
    margin-bottom: 1.875rem;
  }
}

@media (min-width: 64em) {
  .footer__links.col2 {
    grid-area: links2;
  }
}

.footer__links a {
  line-height: 2.25;
  -webkit-transition: color 150ms ease-in-out;
  transition: color 150ms ease-in-out;
}

.footer__links a:hover {
  color: #31d35c;
}

@media (min-width: 64em) {
  .footer__cta {
    grid-area: cta;
    text-align: right;
    -ms-grid-column-align: end;
        justify-self: end;
  }
}

@media (max-width: 63.9375em) {
  .footer__cta a.button {
    margin-bottom: 1.875rem;
  }
}

.footer__copyright {
  font-size: 0.8125rem;
  color: #9698a6;
}

@media (min-width: 64em) {
  .footer__copyright {
    grid-area: copyright;
    -ms-flex-item-align: end;
        -ms-grid-row-align: end;
        align-self: end;
    -ms-grid-column-align: end;
        justify-self: end;
  }
}

</style>

<script>
  export default {
    mounted() {
    }  
  }
</script>
