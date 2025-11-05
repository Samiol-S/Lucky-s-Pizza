<script>
  import Review from "./Review.svelte";


</script>

<div class="reviews-container d-grid justify-content-center align-items-center">
  <h2 class="headline css-h2 text-center">What Our <span style="color: var(--color-accent);">Guests</span> are Saying</h2>

  <div class="mb-5 d-flex justify-content-center">
    <Review text="Lucky's Pizza Gardena is the BEST PIZZA in the neighborhood . Better than Pizza Hut , Papa John's etc.. if your in the area you need to try Lucky's Pizza . They also got the BEST wings !!!" name="Nicholas"/>
  </div>

  <div class="bottom-grid">
    <Review text="Pizza is fire. Employees have a nice and pleasant attitude, very friendly. Customer service is on point too. Pizza is incredible." name="Oscar"/> 

    <Review text="Very good cooking, it's not greasy, it's juicy, I tried a personal, jalapeño, pineapple, pepperoni, it's a well-made pizza, the edges are crispy recommended." name="pascual j"/>

  </div>

</div>

<style>
  .reviews-container {
    background-image: url('/images/reviews_background.webp');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    padding-block: 4rem;
    padding-inline: 4rem;
  }

  .headline {
    padding-bottom: 4rem;
  }

  .bottom-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;

    justify-content: center;

    column-gap: 3rem;
  }

  @media(max-width: 819.99px) {
    .bottom-grid {
      grid-template-columns: 1fr;
    
      row-gap: 3rem;
    }
  }

  @media(max-width: 538px) {
    .headline {
      max-width: 18rem;

      justify-self: center;
      align-self: center;
    }
  }

  @media(max-width: 425px) {
    .reviews-container {
      padding-inline: 1rem;
    }
  }

</style>