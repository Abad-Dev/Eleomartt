<script>
  import EquipmentCard from "../components/EquipmentCard.svelte";

  import Ptl from "../assets/images/soluciones/Recurso-5.webp"
  import Wms from "../assets/images/soluciones/Recurso-6.webp"
  import Ptw from "../assets/images/soluciones/Recurso-7.webp"
  import CartPicking from "../assets/images/soluciones/Recurso-8.webp"
  import Automatizacion from "../assets/images/soluciones/Recurso-10.webp"
  import Guias from "../assets/images/soluciones/Recurso-11.webp"
  import Consultoria from "../assets/images/soluciones/Recurso-100.webp"

  let equipos = [
    {
      src: Ptl,
      title: "PUT TO LIGHT - PTL",
      descripcion: "Luz y pantallas que guían el picking y la clasificación. Precisión y velocidad en cada paso.",
      url: "https://muvumcorp.com/services/muv-put-to-light-ptl/"
    },
    {
      src: Wms,
      title: "WMS",
      descripcion: "Sistema en la nube para gestionar tu almacén de principio a fin. Control total, menos errores y más eficiencia en tiempo real.",
      url: "https://muvumcorp.com/services/muv-wms/"
    },
    {
      src: Ptw,
      title: "PUT TO WALL e-commerce",
      descripcion: "Clasificación semiautomatizada ideal para pedidos pequeños. Orden y eficiencia.",
      url: "https://muvumcorp.com/services/muv-put-to-wall/"
    },
    {
      src: CartPicking,
      title: "Cart Picking",
      descripcion: "Picking simultáneo con carros inteligentes y guiado por luz. Más rápido, menos errores.",
      url: "https://muvumcorp.com/services/muv-cart-picking/"
    },
    {
      src: Ptl,
      title: "WCS Sorters",
      descripcion: "Automatiza la distribución con sorters inteligentes. Menos costos, más control.",
      url: "https://muvumcorp.com/services/muv-wcs-sorters/"
    },
    {
      src: Automatizacion,
      title: "Automatización",
      descripcion: "Soluciones hechas a la medida para transformar tu logística con tecnología 4.0.",
      url: "https://muvumcorp.com/services/muv-automatizacion/"
    },
    {
      src: Guias,
      title: "Guías",
      descripcion: "Genera las guías automáticamente cuando el pedido está listo, sin intervención manual.",
      url: "https://muvumcorp.com/services/guias/"
    },
    {
      src: Consultoria,
      title: "Consultoría",
      descripcion: "Evaluamos tus operaciones logísticas para identificar oportunidades de mejora y diseñamos estrategias personalizadas.",
      url: "https://muvumcorp.com/services/muv-consultoria-supply-chain/"
    },
  ]
</script>
<div id="soluciones">
  <h1 class="red word-1 text-center">Soluciones</h1>
  <h1 class="blue word-2 text-center">Disponibles</h1>
<!-- 
  <h4 class="text-center text-uppercase mt-4">Flota de equipos disponibles</h4> -->

  <div class="d-flex flex-wrap gap-5 my-5 align-items-center justify-content-center">
    {#each equipos as equipo} 
      <EquipmentCard 
        imgSrc={equipo.src}
        title={equipo.title}
        descripcion={equipo.descripcion}
        url={equipo.url}
      />
    {/each}

    <!-- <div class="w-100 d-flex justify-content-center">
      <button class="btn-primary">Ver Catálogo Completo</button>
    </div> -->
  </div>
</div>