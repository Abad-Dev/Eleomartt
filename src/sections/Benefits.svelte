<script>
  import BenefitCard from "../components/BenefitCard.svelte";

  let benefits = [
  {
    icon: "arrow-down-up",
    title: "Flexibilidad en planes de renta",
    descripcion: "Elige entre diferentes opciones que se adaptan a las necesidades y presupuesto de tu empresa."
  },
  {
    icon: "wrench",
    title: "Respaldo técnico y mantenimiento garantizado",
    descripcion: "Nuestro equipo especializado asegura el funcionamiento continuo de tus equipos con soporte confiable."
  },
  {
    icon: "truck",
    title: "Disponibilidad inmediata de equipos",
    descripcion: "Accede a la tecnología que necesitas sin esperas, con entrega lista para usarse de inmediato."
  },
  {
    icon: "piggy-bank",
    title: "Ahorro en inversión inicial",
    descripcion: "Reduce costos al evitar grandes desembolsos, pagando solo por lo que realmente utilizas."
  },
  {
    icon: "trophy",
    title: "Experiencia de más de 16 años",
    descripcion: "Más de una década y media brindando soluciones efectivas respaldan nuestra trayectoria y confianza."
  }
]
</script>

<div class="container-fluid">
  <h1 class="blue word-1">Beneficios de alquilar con </h1>
  <h1 class="ps-4 red word-2">JECAUD RENTING</h1>

  <div class="benefits-container gap-5">
    {#each benefits as benefit}
      <BenefitCard icon={benefit.icon} title={benefit.title} descripcion={benefit.descripcion}/>
    {/each}
  </div>
</div>

<style>
  .benefits-container{
    margin: 50px 0;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }
</style>