<script>
    import Main from "../assets/videos/main.mp4";
</script>

<!-- svelte-ignore a11y-media-has-caption -->
<div class="container-fluid">
    <div class="row hero">
        <video muted autoplay loop>
            <source src={Main} type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <div class="col-12 text-overlay ">
            <div class="container d-flex flex-column gap-4">
                <h1 class="main-title w-100">
                    La <span class="red fw-bold">Fuerza</span> que 
                    <br />
                    <span class="red fw-bold">Mueve</span> tu negocio
                </h1>
    
                <span class="text-white d-block fs-4 fw-light mb-3">Optimiza tu operación logística con equipos especializados en renta.</span>
                
                <div class="d-flex justify-content-center">
                    <a href="#contactenos">
                        <button class="btn-primary">
                            Solicita tu Cotización Ahora 
                            <i class="bi bi-arrow-right"></i>
                        </button>
                    </a>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .hero{
        min-height: 700px;
        position: relative;
    }


    video{
        padding: 0;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        z-index: 0;
    }

    .text-overlay{
        background-color: rgba(0, 0, 0, 0.6);
        min-height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        flex-direction: column;
        background-image: url("../assets/dot.png");
        color: white;

        z-index: 1;
    }

    .main-title{
        font-size: 70px; 
        font-weight: 500;
    }

    @media screen and (max-width: 768px) {
        .hero{
            min-height: 580px;
        }
        .main-title{
            font-size: 50px; 
            font-weight: 700;
        }
    }
</style>

