<script>
  import { onMount } from "svelte";
  import Cta from "./Cta.svelte";
  import { animate, scroll } from "motion";

  let img = $state();

  onMount(() => {
    const animation = animate(
      img,
        { backgroundPositionY: ["0%", "100%"],
          transform: ["translateY(10px)", "translateY(-10px)"]
        },
      
      { duration: 1, easing: "linear" }
    );

    scroll(animation, {
      target: img,                // the element to watch
      axis: "y",
      offset: ["start end", "end start"], 
    });

  })

</script>

<div class="about-container">
  <div class="about-sub-container">

    <div bind:this={img} class="d-flex justify-content-center about-image item-2">
      <!-- <div class="about-image"></div> -->
    </div>

    <div class="left-side">
      <h2 class="css-h2">
        We are Waiting <br>
        For <span  style="color: var(--color-accent);">You!</span>
      </h2>

      <p class="about-p">
        Visit Us at one of our locations : <br>
        &middot; 9030 Owensmouth Ave, <span  style="color: var(--color-accent);"> Canoga Park</span><br>
        &middot; 1373 W Redondo Bch Blvd, <span  style="color: var(--color-accent);">Gardena</span>
      </p>
      <Cta text="Menu"/>
    </div>
      
    
  </div>
</div>

<style>
  .about-container {
    background-color: var(--color-primary);
    padding: 3rem;
    padding-top: 5rem;
    padding-bottom: 15rem;
    
  }

  .about-sub-container {
    display: grid;
    grid-template-columns: minmax(27rem, 30rem) 26rem;
    
    align-items: center;
    justify-content: center;

    column-gap: 5rem;
  }

  .about-p {
    color: #FFF;

    font-family: Poppins;
    font-size: var(--fs-400);
    font-style: normal;
    font-weight: 400;
    line-height: normal;

    max-width:24rem;
    margin-bottom: 2.37rem;
  }

  .about-image {
    background-image: url("/images/about2.png");
    background-size: 125%;
    background-position: center 50%;

    width: 100%;
    height: 24rem;
    border-radius: 9.875rem;
  }

  .left-side {
    max-width: 26rem;
  }


  @media(max-width:1000px) {

    .about-sub-container {
      grid-template-columns: minmax(20rem, 30rem);
      row-gap: 2rem;
    }

    .left-side {
      order: 1;
      margin-bottom: 2rem;
    }

    .item-2 {
      order: 2;
    }
  }

  @media(max-width: 540px) {
    .about-image  {
      height: 18rem;
      border-radius: 6.5rem;
    }
  }

  @media(max-width: 468px) {
    .about-image {

    
      height: 15rem;
    }
  }

  @media(max-width:330px) {
    .about-container {
      padding-left: 4rem;
    }
    .about-image {
      width: 100%;
    }
    .about-sub-container {
      grid-template-columns: minmax(16rem, 30rem);
     
    }
    .about-p {
      font-size: 0.8rem;
    }
  }


</style>  