<script>
    import About from '../assets/images/about.jpg'
</script>

<div class="container-fluid" id="about">
    <div class="row img-container">
        <div class="col-12 col-lg-7 p-3 text-overlay">
            <h1 class="blue word-1">Qui&eacute;nes</h1>
            <h1 class="ps-4 red word-2">Somos</h1>
            <p>
                <span class="fs-4 d-block my-3">
                    <i>"<strong class="red">Especialistas</strong> en soluciones logísticas"</i>
                </span>
                JECAUD RENTING es la unidad de negocio de <strong class="red">JECAUD SERVIS</strong>, con más de 16 años de experiencia en el rubro de maquinaria y logística.
                Ofrecemos a las empresas la posibilidad de acceder a equipos logísticos modernos a través de la renta <strong class="red">flexible, confiable y respaldada por mantenimiento especializado.</strong>
            </p>
        </div>
        <div class="col-12 col-lg-5 d-flex align-items-center justify-content-center p-5 md-p-0">
            <img src={About} alt="..." />
        </div>
    </div>
</div>

<style>
    p{
        font-size: 18px;
        padding: 0 15px;
    }
    img{
        width: 100%;
        height: auto;
        border-radius: 20px;
        box-shadow: 1px 1px 11px 0px var(--ele-red);
    }
    .img-container{
        position: relative;
        max-width: 100vw;
    }
    .text-overlay{
        display: flex;
        flex-direction: column;
        justify-content: center;
        background-size: cover;
        z-index: 1;
    }
</style>






