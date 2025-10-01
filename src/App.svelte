<script>
  import NavBar from "./sections/NavBar.svelte";

  import Main from "./sections/Main.svelte";
  import About from "./sections/About.svelte";
  import Contact from "./sections/Contact.svelte";

  import Footer from "./components/Footer.svelte";
  import WhatsApp from "./components/WhatsApp.svelte";
  import Equipment from "./sections/Equipment.svelte";
  import Benefits from "./sections/Benefits.svelte";
  import Sectors from "./sections/Sectors.svelte";
</script>


<NavBar />
<main>
  <Main />
</main>
<div class="container d-flex flex-column gap-5 pt-5" >
  <About />
  <hr />
  <Equipment />
  <hr />
  <Benefits />
  <hr />
  <Sectors />
  <hr />
  <Contact />
</div>
<Footer />
<WhatsApp />


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