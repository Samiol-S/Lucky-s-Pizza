<script>
  import { browser } from "$app/environment";
  import Cta from "./Cta.svelte";
  function navigateToUrl(url) {

    if (browser) { 
      window.location.href = url;
    }

  }
  

  let sideMenu = $state();

  function removeClass() {
  sideMenu.classList.remove('none');
  }
  function addClass() { 
    sideMenu.classList.add('none'); 
  }


</script>

<header>
  <a href="https://linktr.ee/luckyspizzas#405442614" class="nav-item" target="_blank">Menu</a>
  <a class="nav-item nav-start" href="#footer">Contact Us</a>

  <img class="logo nav-start nav-end" src="/images/Luckys_logo.webp" alt="">
  
  <a class="nav-item me-5 nav-end" href="#about1">About Us</a>
  <a href="https://linktr.ee/luckyspizzas#405442614" class="nav-cta ms-4" target="_blank">Order Online</a>

  <button onclick={removeClass} class="side-menu-button">
    <img src="/images/hamburger-menu.png" class="side-menu-image"  alt="side menu button">
  </button>


  
</header>

<div bind:this={sideMenu} class="side-menu none">
  <div class="header">
    <img class="logo2" src="/images/Luckys_logo.webp" alt="">

    <button onclick="{addClass}" class="arrow-button">
      <img class="arrow" src="/images/arrow.png" alt="">
    </button>

  </div>

  <div class="menu-items1">
    <a href="https://linktr.ee/luckyspizzas#405442614" onclick={() => {
      addClass();
    }} class="menu-item text-center"  target="_blank">Menu</a>

    <a onclick="{addClass}" class="menu-item text-center" href="#footer">Contact Us</a>

    <a onclick="{addClass}" class="menu-item end text-center" href="#about1">About Us</a>

    <Cta text="Order Online"/>
  </div>

</div>

<style>
  .none {
    display: none;
  }
  .side-menu {
    z-index: 100;
    position: fixed;
    top:0;
    left:0;
    right:0;
    bottom:0;

    background-color: var(--color-primary);
  }

  header {
    display: flex;
    justify-content: center;  
    align-items: center;



    height: 8.4375rem;
  }
  .nav-item {
    color: #F4C245;

    font-family: Poppins;
    font-size: 1rem;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    text-decoration: none;

    background-color: transparent;
    border:none;
  }

  .nav-item:hover {
    opacity: 0.8;
  }

  .nav-cta {
    color: #F4C244;

    font-family: Poppins;
    font-size: 1rem;
    font-style: normal;
    font-weight: 500;
    line-height: normal;

    text-decoration-line: underline;
    text-decoration-style: solid;
    text-decoration-skip-ink: auto;
    text-decoration-thickness: 9%; 
    text-underline-offset: 25%; 
    text-underline-position: from-font;

    background: none;
    border:1px solid #F4C244;


    padding-inline:1.44rem;
    padding-block: 1.19rem;
  }

  .nav-cta:hover {
    opacity: 0.8;
  } 

  .nav-start{
    margin-left: 5rem;
  }
  .nav-end{
    margin-right: 5rem;
  }
  .logo {
    width: 7.8125rem;
    height: 5.1875rem;
    
  }


  .side-menu-button {
    display:none;
    background-color: transparent;
    border: none;
  }
  .side-menu-image{
    width: 2.5rem;
    height: 2.5rem;
    margin-right: 5rem;
  }


  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    padding-block: 2rem;
    padding-inline: 3rem;
  }

  .logo2 {
    width: 7.8125rem;
    height: 5.1875rem;
    
  }
  .arrow {
    width: 2.5rem;

  }

  .arrow-button {
    background-color: var(--color-accent);
    padding-block: 0.4rem;
    padding-inline: 0.5rem;

    border: none;
    border-radius: 5px;

  }

  .menu-items1 {
    padding-top: 4rem;
    display: flex;
    flex-direction: column;

    align-items: center;
  }

  .menu-item {
    margin-bottom: 1rem;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid #4C4C4C;
    width:15rem;
    padding-bottom: 1rem;

    color: #F4C244;
    font-family: Poppins;
    font-size: 1.5rem;
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    text-decoration: none;
    cursor: pointer;
  }

  .end {
    margin-bottom: 4rem;
  }

  
  @media(min-width: 900px) {
    .side-menu  {
      display: none !important; 
    }
  }




  /* media queries */

  @media(max-width: 900px) {
    .nav-item,
    .nav-cta{
      display: none;
    }

    header {
      justify-content: space-between;
    }
    .nav-start {
      margin-left:5rem;
    }
    .nav-end {
      margin-right:0rem;
    }

    .side-menu-button{
      display:unset;
    }
  }

  @media(max-width:576px) {
    .nav-start {
      margin-left:2rem;
    }
    .side-menu-image{
      margin-right: 2rem;
    }
  }

</style>