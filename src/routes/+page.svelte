<script>
  import About1 from "$lib/components/About1.svelte";
  import About2 from "$lib/components/About2.svelte";
  import About3 from "$lib/components/About3.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import Gallery from "$lib/components/Gallery.svelte";
  import Hero from "$lib/components/Hero.svelte";
  import Menu from "$lib/components/Menu.svelte";
  import Reviews from "$lib/components/Reviews.svelte";

  


</script>

<svelte:head>
  <title>
    Lucky's Pizza
  </title>
</svelte:head>

<main>
  <Hero/>
  <Menu/>
  <About1/>
  <Gallery/>
  <About2/>
  <Reviews/>
  <About3/>
  <Footer/>
</main>

