<script>
  import { browser } from "$app/environment";
    import { animate, scroll } from "motion";
    import { onMount } from "svelte";

  let { itemName, itemDescription, image } = $props();

  function navigateToUrl(url) {

    if (browser) { 
      window.location.href = url;
    }

  }

  let img = $state();

  onMount(() => {
    const animation = animate(
      img,
        { transform: ["rotate(0deg)", "rotate(40deg)"]},
      
      { duration: 1, ease: "linear"}
    );

    scroll(animation, {
      target: img,                // the element to watch
      axis: "y",
      offset: ["start end", "end start"], 
    });

  })
</script>

<div class="item">

  <img bind:this={img} class="item-image" src="../../images/{image}.png" alt="">

  <h3 class="css-h3 item-name">{itemName}</h3>

  <p class="item-description text-center">{itemDescription}</p>

  <button onclick={navigateToUrl("https://linktr.ee/luckyspizzas#405442614")} class="view-button">
    View
  </button>

</div>

<style>
  .item {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    max-width: 23rem;
    

  }

  .item-image {
    width:18rem;
  }
  .item-name {
    font-size: 1.5rem;
    font-family: Poppins;
    color: var(--color-accent)
  }
  .item-description {
    color: white;
    max-width:12.5rem;
  }

  .view-button {
    transition: background-color 0.2s , color 0.2s; 

    background-color: var(--color-accent);
    border: solid var(--color-accent) 1px;
    padding-inline: 1.25rem;
    padding-block: 0.44rem;

    color: #000;

    font-family: Poppins;
    font-size: 1rem;
    font-style: normal;
    font-weight: 500;
    line-height: normal;

  }

  .view-button:hover {
    transition: background-color 0.2s , color 0.2s; 

    background-color: var(--color-primary);
    color: var(--color-accent);
    
  } 

  @media(max-width: 1115px) {
    .item-image {
      width:22rem;
    }
    .item-name {
      font-size: 2rem;
    }

  }

  @media(max-width: 767px) {
    .item-image {
    width:18rem;
  }
  .item-name {
    font-size: 1.5rem;
  }
  }

  @media(max-width: 346px) {
    .item-image {
      width:16rem;
    }
  }


</style>