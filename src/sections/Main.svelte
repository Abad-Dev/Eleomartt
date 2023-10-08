<script>
    import Main from "../assets/main.mp4";
    import MainOff from "../assets/main.ogg";
</script>

<!-- svelte-ignore a11y-media-has-caption -->
<div class="container-fluid">
    <div class="row hero">
        <video muted autoplay loop>
            <source src={Main} type="video/mp4">
            <source src={MainOff} type="video/ogg">
            Your browser does not support the video tag.
        </video>
        <div class="col-12 text-overlay">
            <h1 class="main-title">Producción Audiovisual <br> de <span class="red">Alta</span> Calidad</h1>
            <p>Confianza, calidad, buen precio y eficiencia en una misma empresa.</p>
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
        font-weight: 700;
    }

    @media screen and (max-width: 768px) {
        .main-title{
            font-size: 50px; 
            font-weight: 700;
        }
    }
</style>

