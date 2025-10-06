<script>
  import Alimentos from "../assets/images/sectores/alimentos.png";
  import Automotriz from "../assets/images/sectores/AUTOMOTRIZ.png";
  import Construccion from "../assets/images/sectores/CONSTRUCCION.png";
  import Ecommerce from "../assets/images/sectores/ecommerce.png";
  import Retail from "../assets/images/sectores/retail.png";
  import Textil from "../assets/images/sectores/textil.png";
  import Farmaceutico from "../assets/images/sectores/FARMACEUTICO.png";

  let sectors = [
  {
    img: Ecommerce,
    title: "E-commerce",
    descripcion: "Agiliza la gestión de pedidos, inventario y envíos para mejorar la experiencia de tus clientes en línea."
  },
  {
    img: Retail,
    title: "Retail y supermercados",
    descripcion: "Optimiza la reposición y control de productos, garantizando eficiencia en el punto de venta."
  },
  {
    img: Textil,
    title: "Textil y moda",
    descripcion: "Gestiona tu producción y stock de forma inteligente, adaptándote rápidamente a las tendencias del mercado."
  },
  {
    img: Alimentos,
    title: "Alimentos y bebidas",
    descripcion: "Asegura la trazabilidad, control de calidad y cumplimiento de normativas en cada etapa de la cadena."
  },
  {
    img: Farmaceutico,
    title: "Farmacéutico",
    descripcion: "Mantén el control total sobre tus productos sensibles con soluciones seguras y confiables."
  },
  {
    img: Automotriz,
    title: "Automotriz",
    descripcion: "Optimiza la gestión de partes, ensambles y logística con tecnología de alto rendimiento."
  },
  {
    img: Construccion,
    title: "Construcción",
    descripcion: "Coordina maquinaria, materiales y personal para garantizar proyectos eficientes y bien gestionados."
  }
]
</script>

<div class="container-fluid" id="sectores">
  <h1 class="blue word-1 text-center">Sectores</h1>
  <h1 class="red word-2 text-center">Atendidos</h1>

  <div class="container-fluid d-flex justify-content-center align-items-center mt-5">
    <div class="sector-container">
    {#each sectors as sector}
      <div class="sector">
        <div class="icon-container">
          <div class="icon">
            <img src={sector.img} alt="...">
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
    padding: 0;
    gap: 45px;
  }


  .sector {
    border-color: inherit;
    height: 320px;
    width: 320px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    text-align: center;
    padding: 30px;
    background-color: white;
    box-shadow: 0px 0px 10px 0px #32323286;
    border-radius: 20px;
    transition-duration: .4s;
  }

  .sector:hover{
    transform: translateY(-5px);
    box-shadow: 0px 0px 25px 0px var(--ele-red);
  }

  .icon-container{
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .icon, .icon > img {
    width: 100px;
    height: 100px;
    color: var(--ele-red);
    border-radius: 100%;
    position: relative;

    display: grid;
    place-items: center;
    font-size: 40px;

    margin-bottom: 5px;
  }
</style>