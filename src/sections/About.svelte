<script>
    import About from "../assets/about.jpg";
</script>

<div class="container-fluid" id="about">
    <div class="row img-container">
        <div class="col-7 text-overlay">
            <h1 class="blue word-1">Sobre</h1>
            <h1 class="ps-4 red word-2">Nosotros</h1>
            <p class="mb-5">
                Somos una productora audiovisual dedicada a crear contenido único, cautivador y de alta calidad. Permítanme contarles un poco más sobre quiénes somos y qué hacemos.
                Nuestro principal objetivo es transformar ideas en imágenes en movimiento.
                Contamos con un equipo de profesionales apasionados por contar historias a través del poder de la imagen y el sonido.
            </p>
            <h3>Luis A. Martínez Torres</h3>
            <small>PRODUCTOR GENERAL</small>
        </div>
        <img src={About} alt="..." class="d-none d-sm-block"/>
    </div>
</div>

<style>
    #about{
        padding-top: 88px;
        margin-top: -88px;
    }
    p{
        font-size: 18px;
        padding: 0 15px;
    }
    img{
        position: absolute;
        right: 0px;
        bottom: 0px;
        width: auto;
        height: 100%;
        z-index: -1;
    }
    .img-container{
        position: relative;
        max-width: 100vw;
    }
    .text-overlay{
        padding-top: 50px;
        padding-bottom: 30px;
        padding-left: 0px;
        padding-right: 0px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        background-size: cover;
        z-index: 1;
    }

    @media screen and (max-width: 1400px) {
        img{
            right: 0px;
            bottom: 15px;
        }
    }
    @media screen and (max-width: 1200px) {
        p{
            font-size: 16px;
        }
        img{
            right: 0px;
            bottom: 20px;
        }
        .text-overlay{
            padding-left: 0px;
        }
    }
    @media screen and (max-width: 991px) {
        .text-overlay{
            padding: 30px;
        }
        img{
            height: 70%;
            top: 50%;
            transform: translate(0, -50%);
        }
    }

    @media screen and (max-width: 768px) {
        .text-overlay{
            background-image: url("../assets/about-light.jpg");
            background-size: cover;
            background-position: center center;
            text-align: center;
            padding: 100px 15px;
        }
        img{
            display: none !important;
        }
        .text-overlay{
            flex-basis: 100%;
        }
    }
</style>






