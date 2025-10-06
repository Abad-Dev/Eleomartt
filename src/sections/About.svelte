<script>
    import About from '../assets/images/quienes-somos.jpg'

    const verPDF = () => {
        const url = "docs/PRESENTACION_CORPORATIVA_MUVUM_2025.pdf";
        window.open(url, "_blank", "noopener,noreferrer");
    };
</script>

<div class="container-fluid" id="about">
    <div class="row img-container">
        <div class="col-12 col-lg-6 p-3 text-overlay">
            <h1 class="blue word-1">Qui&eacute;nes</h1>
            <h1 class="ps-4 red word-2">Somos</h1>
            <p>
                <!-- <span class="fs-4 d-block my-3">
                    <i>"<strong class="red">Especialistas</strong> en soluciones logísticas"</i>
                </span> -->
                <span style="color: #1AA7E0;" class="fw-bold">MUvum</span> es una marca global con más de 20 años de experiencia, dedicada a diseñar e integrar soluciones estratégicas para la cadena de abastecimiento.
                <br /><br />
                Con presencia en <strong class="red">+7 países de Latinoamérica</strong>, ha optimizado más de 80 centros de distribución y atiende a miles de tiendas cada día.
            </p>

            <button class="btn-primary mt-3 text-align-center justify-content-center mx-3" on:click={verPDF}>
                Ver Presentación Corporativa MUvum 2025

                <i class="bi bi-arrow-right"></i>
            </button>
        </div>
        <div class="col-12 col-lg-6 d-flex align-items-center justify-content-center p-5 md-p-0">
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






