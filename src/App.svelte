<script>
  import NavBar from "./sections/NavBar.svelte";
  import Main from "./sections/Main.svelte";
  import About from "./sections/About.svelte";
  import Works from "./sections/Works.svelte";
  import Services from "./sections/Services.svelte"
</script>


<NavBar />
<main>
  <Main />
</main>
<div class="container">
  <About />
  <Works />
  <Services />
</div>

<style>
  main{
    padding: 88px 0 0 0;/* This is the height of the image of the logo in the navbar */
  }

  @media screen and (max-width: 768px) {
    .container{
      padding: 0;
    }
  }
</style>