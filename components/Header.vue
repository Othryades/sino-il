<template>
    <header class="header">
      <div class="overlay has-fade"></div>

      <nav class="container container--pall flex flex-jc-sb flex-ai-c">
       <nuxt-link to="/" class="header__logo">
          <img src="~/assets/images/logo.png" alt="logo" title="main logo"  loading="lazy"/>
        </nuxt-link>

        <a id="btnHamburger" href="#" class="header__toggle hide-for-desktop">
          <span></span>
          <span></span>
          <span></span>
        </a>

        <div class="header__links hide-for-mobile">
          <nuxt-link to="/" class="first__link">Home</nuxt-link>                    
          <div class="dropdown">
            <button class="dropbtn">Services</button>
            <div class="dropdown-content">
              <nuxt-link to="/services/talent-program">Talent program</nuxt-link>
              <nuxt-link to="/services/governmental-grants">Govermental grants - Hangzhou</nuxt-link>
              <nuxt-link to="/services/FA-business">FA-business</nuxt-link>
              <nuxt-link to="/services/marketing">Marketing</nuxt-link>
            </div>
          </div>
          <nuxt-link to="/about-us" class="first__link">About Us</nuxt-link>
          <nuxt-link to="/contact" class="first__link">Contact</nuxt-link>
        </div>
        <a href="#" class="button header__cta hide-for-mobile">Forecast 2021</a>
      </nav>

      <div class="header__menu has-fade">
        <nuxt-link to="/" class="first__link">Home</nuxt-link>   
        <nuxt-link to="/services/talent-program">Talent program</nuxt-link>
        <nuxt-link to="/services/governmental-grants">Govermental grants</nuxt-link>
        <nuxt-link to="/services/FA-business">FA-business</nuxt-link>
        <nuxt-link to="/services/marketing">Marketing</nuxt-link>                        
        <nuxt-link to="/about-us" class="first__link">About Us</nuxt-link>
        <nuxt-link to="/contact" class="first__link">Contact</nuxt-link>
      </div>
    </header>
</template>

<style>


/* header */
.header {
  position: relative;
  z-index: 1;
}

.header.open .header__toggle > span:first-child {
  -webkit-transform: rotate(45deg);
          transform: rotate(45deg);
}

.header.open .header__toggle > span:nth-child(2) {
  opacity: 0;
}

.header.open .header__toggle > span:last-child {
  -webkit-transform: rotate(-45deg);
          transform: rotate(-45deg);
}

.header .overlay {
  opacity: 0;
  position: fixed;
  top: 0px;
  right: 0px;
  bottom: 0px;
  left: 0px;
  background-image: -webkit-gradient(linear, left top, left bottom, from(#2d314d), to(transparent));
  background-image: linear-gradient(#2d314d, transparent);
}

.header nav {
  position: relative;
  background-color: white;
  padding-top: 1.0625rem;
  padding-bottom: 1.0625rem;
}

.header__logo img {
  /* width: 8.8125rem;
  height: 1.375rem; */
}

.header__toggle > span {
  display: block;
  width: 26px;
  height: 2px;
  background-color: #2d314d;
  -webkit-transition: all 300ms ease-in-out;
  transition: all 300ms ease-in-out;
  -webkit-transform-origin: 3px 1px;
          transform-origin: 3px 1px;
}

.header__toggle > span:not(:last-child) {
  margin-bottom: 5px;
}

.header__menu {
  position: absolute;
  width: calc(100% - 3rem);
  left: 50%;
  -webkit-transform: translateX(-50%);
          transform: translateX(-50%);
  background: white;
  margin-top: 1.5rem;
  padding: 1.625rem;
  border-radius: 5px;
}

.header__menu a {
  display: block;
  padding: 0.625rem;
  color: #2d314d;
  text-align: center;
}

.header__links a {
  position: relative;
  font-size: 0.875rem;
  color: #9698a6;
  -webkit-transition: color 300ms ease-in-out;
  transition: color 300ms ease-in-out;
}

.header__links a:not(:last-child).first__link {
  margin-right: 32px;
}

.header__links a.first__link::before {
  content: "";
  display: block;
  position: absolute;
  height: 5px;
  left: 0;
  right: 0;
  bottom: -20px;
  background: -webkit-gradient(linear, left top, right top, from(#31d35c), to(#2bb7da));
  background: linear-gradient(to right,#2025bb, #e42a2a);
  opacity: 0;
  -webkit-transition: opacity 300ms ease-in-out;
  transition: opacity 300ms ease-in-out;
}

.header__links a:hover {
  color: #2d314d;
}

.header__links a:hover::before {
  opacity: 1;
}

.dropbtn {
    font-size: 0.875rem;
    color: #9698a6;
  border: none;
  background-color: unset;
}

.dropdown {
  position: relative;
  display: inline-block;
  margin-right: 32px;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  min-width: 245px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #ddd;}

.dropdown:hover .dropdown-content {display: block;}

/* .dropdown:hover .dropbtn {background-color: #3e8e41;} */
</style>


<script>
export default {
mounted() {

  const btnHamburger = document.querySelector('#btnHamburger');
  const body = document.querySelector('body');
  const header = document.querySelector('.header');
  const overlay = document.querySelector('.overlay');
  const fadeElems = document.querySelectorAll('.has-fade');

  btnHamburger.addEventListener('click', function(){
    console.log('click hamburger');

    if(header.classList.contains('open')){ // Close Hamburger Menu
      body.classList.remove('noscroll');
      header.classList.remove('open');    
      fadeElems.forEach(function(element){
        element.classList.remove('fade-in');
        element.classList.add('fade-out');
      });
      
    }
    else { // Open Hamburger Menu
      body.classList.add('noscroll');
      header.classList.add('open');
      fadeElems.forEach(function(element){
        element.classList.remove('fade-out');
        element.classList.add('fade-in');
      });

    }  
  });

}  
}
</script>
