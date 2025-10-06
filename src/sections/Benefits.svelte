<script>
  import BenefitCard from "../components/BenefitCard.svelte";

  let benefits = [
  {
    icon: "bar-chart",
    title: "+80% productividad",
    descripcion: "Aumenta la eficiencia operativa de tu empresa gracias a herramientas optimizadas y procesos automatizados."
  },
  {
    icon: "shield-check",
    title: "Reducción significativa de errores",
    descripcion: "Minimiza fallas humanas y operativas mediante controles automatizados y flujos de trabajo inteligentes."
  },
  {
    icon: "clock",
    title: "Optimización de espacio y tiempos",
    descripcion: "Aprovecha mejor tus recursos físicos y temporales con soluciones diseñadas para máxima eficiencia."
  },
  {
    icon: "eye",
    title: "Visibilidad en tiempo real",
    descripcion: "Monitorea y analiza cada proceso al instante para una toma de decisiones más ágil y precisa."
  },
  {
    icon: "layers",
    title: "Escalabilidad y flexibilidad",
    descripcion: "Adapta el sistema al crecimiento de tu negocio sin perder rendimiento ni estabilidad."
  },
  {
    icon: "person-raised-hand",
    title: "Soporte local en Perú",
    descripcion: "Contamos con asistencia técnica y atención personalizada dentro del país, siempre cerca de ti."
  }
]

</script>

<div class="container-fluid" id="beneficios">
  <h1 class="blue word-1" style="line-height: 30px;">Beneficios de <strong style="color: #1AA7E0;">MUvum</strong></h1>
  <h1 class="ps-4 word-2">con <strong class="red">JECAUD SERVIS</strong></h1>

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