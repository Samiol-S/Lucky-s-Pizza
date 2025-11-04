<script>
  import { browser } from "$app/environment";
  import { goto } from "$app/navigation";
  
  let { text } = $props();

  function navigateToUrl(url) {

    if (browser) { 
      window.location.href = url;
    }

  }
  
</script>

<div class="button-container px-1  d-flex justify-content-center align-items-center">
  <button onclick={navigateToUrl("https://linktr.ee/luckyspizzas#405442614")} class='cta p-0 m-0'>{text}</button>
</div>

<style>
  .button-container{
    border: 1px solid #F4C244;
    width: 8.9125rem;
    height: 3.725rem;
    transition: scale 0.3s ease;
  }
  .cta{
    transition: background-color 0.2s , color 0.2s;

    background-color:#F4C244;
    border: solid var(--color-accent) 1px;
    width: 8.925rem;
    height: 3.125rem;
    
    color: #000;
    font-family: Poppins;
    font-size: 1rem;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
  }

  .cta:hover {
    transition: background-color 0.2s , color 0.2s; 

    background-color: var(--color-primary);
    color: var(--color-accent);
    
  }
  
  .cta:active {
    opacity:0.8;
  }


  /* .button-container:hover {
    transition: scale 0.3s ease;
    scale: 1.1;
  }
   */
</style>