<script>
    let imagesNames = [
        'betara',
        'bitel',
        'busser',
        'DamianYElToyo',
        'dvieri',
        'Fratelli',
        'goldenPalace',
        'hiraoka',
        'hudbay',
        'lg',
        'MinisterioDeSalud',
        'mitsui',
        'nefusac',
        'Nestle',
        'oppo',
        'peruanosEnElMundo',
        'perubus',
        'ransa',
        'senati'
    ]
</script>

<div id="clients">
    <h1 class="blue word-1 text-center">Nuestros</h1>
    <h1 class="red word-2 text-center uld">Clientes</h1>

    <div class="container-fluid">
        <div class="row justify-content-center">
            {#each imagesNames as name}
            <div class="col-6 col-md-4 col-lg-3 image-container">
                <img src={"/src/assets/clientes_eleomartt/"+name+".png"} alt="">
            </div>
            {/each}
        </div>
    </div>
</div>


<style>
    #clients{
        padding: 100px 0;
    }

    .image-container{
        display: flex;
        align-items: center;
        justify-content: center;
        
        padding: 15px;
    }
    img{
        max-width: 100%;
    }
</style>