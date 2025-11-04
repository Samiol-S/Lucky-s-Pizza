<script>
  let { text, name } = $props();
</script>

<div class="review ">
  <img class="image" src="/images/five_stars.png" alt="">
  <p class="comment">{text}</p>
  <p class="person">~ {name}</p>
  
</div>

<style>
  .image {
    width: 7.6rem;
  }
  .review {
    background-color: #111;
    max-width: 29.25rem;

    padding-top: 0.2rem;
    padding-inline: 3rem;
    padding-bottom: 1rem;
    
    border-radius: 1.5rem;

    justify-self: center;
    
  }
  .comment {
    color: #fff;
    font-family: Poppins;
    font-size: 1.0625rem;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }
  .person {
    opacity: 0.64;
    color: #FFF;
    font-family: Poppins;
    font-size: 1.25rem;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }

  @media(max-width:525px) {
    .comment {
      font-size: 0.825rem;
    }

    .person {
      font-size: 0.8rem;
    }
  }

  @media(max-width:380px) {
    .review {
      padding-top: 0.2rem;
      padding-inline: 2rem;
      padding-bottom: 1.3rem;
    }
  }
</style>