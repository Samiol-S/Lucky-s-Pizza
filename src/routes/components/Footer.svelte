<script>
  import { browser } from "$app/environment";

  function navigateToUrl(url) {

    if (browser) { 
      window.location.href = url;
    }

  }
</script>

<div class="footer" id="footer">
  <div class="d-flex justify-content-center align-items-center">
    <img class="logo" src="/images/Luckys_logo.png" alt="">

  </div>

  <div class="details">
    <div>
      <p class="title">Links</p>
      <p>
        <a href="# ">Home</a> <br>
        <button onclick={navigateToUrl("https://linktr.ee/luckyspizzas#405442614")} class="a-button">Menu</button> <br>
        <a href="#about1">About Us</a>
      </p>
    </div>
    
    <div class="ms-4">
      <p class="title">Contacts</p>
      <p>
        310.853.3419 - <span style="color:var(--color-accent);">Canoga Park</span> <br>
        310.344.2610 - <span style="color:var(--color-accent);">Gardena</span> <br>
        <button onclick={navigateToUrl("https://www.instagram.com/luckyspizzas/?hl=en")}
          class="a-button" >Instagram</button>
      </p>    
    </div>
  
  </div>

</div>

<style>

  a {
    color: white;
    font-size: var(--fs-300);


    text-decoration-line: underline;
    text-decoration-style: solid;
    text-decoration-skip-ink: auto;
    text-decoration-thickness: auto;
    text-underline-offset: 17%; /* 2.72px */
    text-underline-position: from-font;
  }

  .footer {
    padding: 4rem;
    background-color: #000000;
  
    display: grid;
    grid-template-columns: 1fr 1fr;
    
  }
  
  .logo {
    width: 15.8125rem;
  }

  .details {
    display: flex;
    justify-content: start;
    align-items: center;

    color: white;

    font-family: Poppins;
    font-size: var(--fs-300);
    
  }

  .title {
    color: var(--color-accent);
    font-size: var(--fs-400);

    font-family: Poppins;
  }

  .a-button {
    background-color: transparent;
    border: none;
    text-decoration: underline;
    color: white;

    padding:0;
  }

  @media(max-width: 1000px) {
    .logo {
      width: 10.8125rem;
    }
  }
  @media(max-width: 684px) {
    .footer {
      padding: 2rem;
    }

  }

  @media(max-width: 618px) {
    .footer {
      grid-template-columns: 1fr;
      row-gap: 2rem;
      justify-content: center; 
      align-items: center;
    }

    .details {
      justify-content: center;
      padding-bottom: 2rem;

      

    }

  }

  @media(max-width: 350px) {
    .details,
    a {
      font-size: 0.7rem;
    }
  }

    
</style>