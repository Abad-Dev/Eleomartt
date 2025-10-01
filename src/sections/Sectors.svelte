<script>
  let sectors = [
    {
      icon: "box-seam",
      title: "Centros de distribución",
      descripcion: "Optimiza tus operaciones y mantén el flujo constante de tus productos."
    },
    {
      icon: "building-gear",
      title: "Fábricas e industrias",
      descripcion: "Apoya la productividad con equipos confiables en cada etapa de tu producción."
    },
    {
      icon: "shop",
      title: "Retail y supermercados",
      descripcion: "Facilita la gestión de inventario y garantiza la atención ágil a tus clientes."
    },
    {
      icon: "truck",
      title: "Operadores logísticos",
      descripcion: "Mejora la cadena de suministro con soluciones listas para cualquier desafío."
    },
  ]
</script>

<div class="container-fluid" id="sectores">
  <h1 class="blue word-1 text-center">Sectores</h1>
  <h1 class="red word-2 text-center">Que Atendemos</h1>

  <h4 class="text-center text-uppercase mt-4"><i>"<strong class="red">Soluciones</strong> para tu industria</i>"</h4>

  <div class="container-fluid d-flex justify-content-center align-items-center mt-5">
    <div class="sector-container">
    {#each sectors as sector}
      <div class="sector">
        <div class="icon-container">
          <div class="icon">
            <i class={"bi bi-" + sector.icon}></i>
          </div>
        </div>

        <div class="text-container">
          <h4 class="red">{sector.title}</h4>
          <p class="text-secondary mt-2">{sector.descripcion}</p>
        </div>
      </div>
    {/each}
  </div>
  </div>
  
</div>

<style>
  .sector-container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 604px;
    padding: 0;
    border: 2px solid #c5c5c5;
    border-radius: 20px;
    overflow: hidden;
  }

  @media (min-width: 768px) {
  .sector-container > div:nth-child(1) { border-width: 0 1px 1px 0; }
  .sector-container > div:nth-child(2) { border-width: 0 0 1px 1px; }
  .sector-container > div:nth-child(3) { border-width: 1px 1px 0 0; }
  .sector-container > div:nth-child(4) { border-width: 1px 0 0 1px; }
  }

  @media (max-width: 768px) {
    .sector-container > div { border-width: 0 0 1px 0;}
    .sector-container > div:nth-child(4) { border-width:0; }
  }

  .sector {
    border-style: solid;
    border-color: inherit;
    height: 300px;
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    text-align: center;
    padding: 30px;
  }

  .icon-container{
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .icon {
    width: 100px;
    height: 100px;
    color: var(--ele-red);
    border-radius: 100%;
    position: relative;

    display: grid;
    place-items: center;
    font-size: 40px;
  }
</style>