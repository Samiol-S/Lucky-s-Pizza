<script>
    import { onMount } from "svelte";


  import { animate, scroll } from "motion";
    import Cta from "./Cta.svelte";


  let img = $state();

  onMount(() => {
    const animation = animate(
      img,
        { backgroundPositionY: ["0%", "100%"],
          transform: ["translateY(10px)", "translateY(-10px)"]
        },
      
      { easing: "linear" }
    );

    scroll(animation, {
      target: img,                
      offset: ["start end", "end start"], 
    });

  })

</script>

<div class="about-container" id="about1">
  <div class="about-sub-container">
    <div class="left-side">
      <h2 class="css-h2">
        What Makes Us <br>
        <span  style="color: var(--color-accent);">Different</span>

      </h2>
      <p class="about-p">
        Loved by locals, <span  style="color: var(--color-accent);">Lucky's Pizza</span> is more than just great food, it's a neighborhood favorite where good people and good <span  style="color: var(--color-accent);">pizza</span> come together every day.
      </p>
      
      <Cta text="Order Online"/>
    </div>
    
    <div bind:this={img} class="d-flex justify-content-center about-image">
      <!-- <div class="about-image"></div> -->
    </div>
    
  </div>
</div>

<style>
  .about-container {
    background-color: var(--color-primary);
    padding: 3rem;
    padding-bottom: 6rem;

  }

  .about-sub-container {
    display: grid;
    grid-template-columns: 26rem minmax(27rem, 30rem);
    
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
    background-image: url("/images/about.png");
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
      margin-bottom: 2rem;
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
  }


</style>  