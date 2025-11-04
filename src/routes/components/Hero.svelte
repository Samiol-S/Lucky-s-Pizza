<script>
  import Cta from "./Cta.svelte";
  import Header from "./Header.svelte";

</script>


<div class="background-image">
  <Header/>
  
  <div class="all-container d-flex align-items-center"> 
    <div class="this-container">
      
      <p class="css-h1 hero-head mb-2">
        For the Love <br>
        of <span class="pizza">Pizza.</span>
      </p>

      <p class="fs-md sub-head">Authentic flavor,<br> baked fresh daily</p>

      <Cta text="Order Online"/>
      
      
    </div>
  </div>
  
</div>



<style>


  .background-image {
    background-image: url("../../images/hero_image.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 0rem ;

    min-height: 43.25rem;
    max-height: 46.25rem;
    height:100vh
    
  }

  .sub-head {
    color: rgba(255, 255, 255, 0.80);
    margin-bottom: 2.5rem;
  }


  .pizza {
    color: var(--color-accent)
  }

  .this-container {
    margin-left: 6.25rem;
    margin-top: 3rem;
  }
  
  .all-container {
    
    height: 28rem;
  }


  @media(max-width: 768px) {
    .this-container {
    margin-left: 4.25rem;
  }
  }

  @media(max-width: 576px) {
    .background-image{
      background-position: -10rem;

    }
    .this-container {
      margin-left: 3.25rem;
    }
    .hero-head{
      margin-bottom:0;
    }
  }
  
  @media(max-width: 450px) {
    .this-container{
      margin-left: 2rem;
      margin-top: 0;
    }
  }

  @media(max-width:370px) {
    .hero-head {
      font-size: 3rem;
      line-height: 1.2;
    }
    .sub-head{
      font-size: 0.875rem;
    }
  }


</style>