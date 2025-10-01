<script>
  import EquipmentCard from "../components/EquipmentCard.svelte";

  import Transpleta from "../assets/images/equipos/transpleta.jpg"
  import Apilador from "../assets/images/equipos/apilador.jpg"
  import Montacargas from "../assets/images/equipos/montacargas.jpg"
  import Trilateral from "../assets/images/equipos/trilateral.jpg"
  import Bateria from "../assets/images/equipos/baterias.jpg"

  let equipos = [
    {
      src: Transpleta,
      title: "Transpaletas Eléctricas",
      subTitle: "transporte interno, ágil y seguro",
      descripcion: "Mueve pallets rápida y fácilmente, reduciendo esfuerzo y aumentando seguridad."
    },
    {
      src: Apilador,
      title: "Apiladores Eléctricos",
      subTitle: "ideal para elevar pallets en espacios reducidos",
      descripcion: "Eleva y coloca pallets con precisión en zonas estrechas, optimizando espacio."
    },
    {
      src: Montacargas,
      title: "Montacargas a Combustión Dual",
      subTitle: "potencia y versatilidad",
      descripcion: "Transporta cargas pesadas con fuerza y flexibilidad, en interiores o exteriores."
    },
    {
      src: Trilateral,
      title: "Trilaterales",
      subTitle: "máximo aprovechamiento de espacio en pasillos estrechos",
      descripcion: "Maniobra en pasillos angostos, accediendo a pallets difíciles y ahorrando espacio."
    },
    {
      src: Bateria,
      title: "Baterías",
      subTitle: "energía confiable para equipos eléctricos",
      descripcion: "Proporciona energía constante y duradera para mantener tus equipos operativos."
    }
  ]
</script>
<div id="equipos">
  <h1 class="blue word-1 text-center">Nuestros</h1>
  <h1 class="red word-2 text-center">Equipos</h1>

  <h4 class="text-center text-uppercase mt-4">Flota de equipos disponibles</h4>

  <div class="d-flex flex-wrap gap-5 my-5 align-items-center justify-content-center">
    {#each equipos as equipo} 
      <EquipmentCard 
        imgSrc={equipo.src}
        title={equipo.title}
        subTitle={equipo.subTitle}
        descripcion={equipo.descripcion}
      />
    {/each}

    <!-- <div class="w-100 d-flex justify-content-center">
      <button class="btn-primary">Ver Catálogo Completo</button>
    </div> -->
  </div>
</div>