<script>

</script>

<div class="gallery-container ">
  <h2 class="css-h2 text-center mb-5">
    Join Our <span class="accent">Community</span> And try out the <span class="accent">Food</span>
  </h2>
  
  <div class="images">
    <img class="image" style="grid-area: box-1" src="/images/gallery/chicken_wings.jpg" alt="chicken wings">
    <img class="image-2" style="grid-area: box-2" src="/images/gallery/wall1.jpg" alt="wall signatures">
    <img class="image" style="grid-area: box-3" src="/images/gallery/wall2.jpg" alt="wall signatures 2">
    <img class="image-4" style="grid-area: box-4" src="/images/gallery/pizza2.jpg" alt="a pizza">
    <img class="image" style="grid-area: box-5" src="/images/gallery/pizza.jpg" alt="a pizza">
    <img class="image-6" style="grid-area: box-6" src="/images/gallery/garlic_bread.jpg" alt="garlic bread">

  </div>
</div>

<style>
  .gallery-container {
    background-color: #111;
    display: grid;
    justify-content: center;
    align-items: center;

    padding: 3rem;
    padding-bottom: 7rem;
  }

  .accent {
    color: var(--color-accent);
  }

  .images {
    display: grid;
    grid-auto-columns: 18.625rem;
    grid-auto-rows: 18.625rem;

    grid-template-areas: 
    "box-1 box-2 box-3 box-4"
    "box-5 box-2 box-6 box-6";

    row-gap: 1rem;
    column-gap: 1rem;

    align-items: center;
    justify-content: center;
  }

  .image {
    width: 18.625rem;
    height: 18.625rem;

    border-radius: 0.3125rem;
  }

  .image-2 {
    width: 18.625rem;
    height: 38.25rem;

    object-fit: cover;
    border-radius: 0.3125rem;

  }

  .image-4 {
    width: 18.625rem;
    height: 18.625rem;
    border-radius: 0.3125rem;
  }
  
  .image-6 {
    width: 38.1875rem; 
    height: 18.625rem;

    object-fit: cover;
    border-radius: 0.3125rem;
  }

  @media (max-width: 1290px) {
    .images {
      grid-template-areas: 
      "box-1 box-2"
      "box-5 box-2"
      "box-3 box-4"
      "box-6 box-6";
    }
  }

  @media (max-width: 920px) {
    .css-h2{
      font-size: 2.25rem;
    }
  }

  @media (max-width: 660px) {
    .css-h2 {
      width: 23rem;
    }

    .images {
      grid-auto-columns: 10.625rem;
      grid-auto-rows: 10.625rem;
    }

    .image {
      height: 10.625rem;
      width: 10.625rem;
    }
    
    .image-2 {
      width: 10.625rem;
      height: 22.25rem;
    }
    
    .image-4 {
      height: 10.625rem;
      width: 10.625rem;
    }

    .image-6 {
      width: 22.325rem;
      height: 10.625rem;
    }

  }

  @media(max-width: 400px) {
    .css-h2 {
      font-size: 1.8rem;
      width: 18rem;
    }

    .images {
      grid-auto-columns: 8.625rem;
      grid-auto-rows: 8.625rem;
    }

    .image {
      height: 8.625rem;
      width: 8.625rem;
    }
    
    .image-2 {
      width: 8.625rem;
      height: 18.25rem;
    }
    
    .image-4 {
      height: 8.625rem;
      width: 8.625rem;
    }

    .image-6 {
      width: 18.325rem;
      height: 8.625rem;
    }
  
    .gallery-container {
      padding-inline: 0.5rem;
    }
  }

</style>