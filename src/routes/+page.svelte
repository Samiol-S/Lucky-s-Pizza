<script>
  import About1 from "./components/About1.svelte";
  import About2 from "./components/About2.svelte";
  import About3 from "./components/About3.svelte";
  import Footer from "./components/Footer.svelte";
  import Gallery from "./components/Gallery.svelte";
  import Hero from "./components/Hero.svelte";
  import Menu from "./components/Menu.svelte";
  import Reviews from "./components/Reviews.svelte";


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

