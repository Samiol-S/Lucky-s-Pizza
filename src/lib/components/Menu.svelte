<script>
  import Item from "./Item.svelte";

  const items = [{
    name: "Pepperoni Pizza",
    description: "Tomato sauce, mozzarella, and slices of spicy pepperoni.",
    image: "Pepperoni"
  }, {
    name: "Margherita Pizza",
    description: "Tomato sauce,  mozzarella, and fresh basil.",
    image: "Margherita"
  }, {
    name: "Napolitana Pizza",
    description: "Thin, soft crust with tomato sauce, fresh mozzarella, and basil.",
    image: "Napolitana"
  }];

</script>


<div class="menu-section">

  <svg
    viewBox="0 -11 1441 44"
    xmlns="http://www.w3.org/2000/svg"
    preserveAspectRatio="none"
    class="hero-wave"
>
    <path
      d="M0 33C572.608 100 887.965 100 1441 33C883.367 -11.2975 567.886 -10.7015 0 33Z"
      fill="currentColor"
    />
  </svg>

  <div class="content">
    <h2 class="css-h2 text-center headline">
      Explore Our menu
    </h2>

    <div class="items">
      
      {#each items as item}
        <Item itemName={item.name} itemDescription={item.description} image={item.image}/>
      {/each}

    </div>
  </div>

</div>


<style>
  .menu-section {
    margin-top: -2rem;
  }

  .headline{
    color: var(--color-accent);
  }

  .hero-wave {
    color: #111;
    width: 100%;
    height: 2rem;

  }
  .content {
    padding-top: 2rem;
    padding-bottom: 6rem;

    background-color: #111;
    border: none;
    
  }


  .items {
    padding-top:2rem;

    display: grid;
    grid-template-columns: repeat(3, 23rem);
    row-gap: 3rem;
    justify-content: center;
  }



  @media(max-width: 1115px) {
    .content {
      padding-top: 4rem;
    }
    .items {

      grid-template-columns: 20rem;
      row-gap: 5.5rem;
    }
  }

  @media(max-width: 767px) {
    .content {
      padding-top:2rem;
    }
    .items {
      row-gap: 4.5rem;
    }
  }
</style>