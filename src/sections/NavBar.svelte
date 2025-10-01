<script>
    import Logo from "../components/Logo.svelte";
    import ShortLogo from "../components/ShortLogo.svelte";

</script>


<nav class="navbar navbar-expand-lg bg-light">
    <div class="container">
        <div class="d-sm-none">
            <ShortLogo />
        </div>
        <div class="d-none d-sm-block">
            <Logo />
        
        </div>
        
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav ms-auto mb-2 mb-lg-0 gap-3">
                <li class="nav-item ">
                    <a class="nav-link" href="#inicio">Inicio</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#about">Nosotros</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#equipos">Nuestro Equipo</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#beneficios">Beneficios</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#sectores">Sectores</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contactenos">Contáctenos</a>
                </li>
                <!-- <li class="nav-item">
                    <a class="nav-link" href="#works">Trabajos</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#services">Servicios</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#clients">Clientes</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#contact">Contáctenos</a>
                </li> -->
            </ul>
        </div>
    </div>
</nav>


<style>
    nav{
        position: fixed !important;
        min-width: 100%;
        padding: 10px;
        background-color: white !important;
        box-shadow: 1px 3px 5px 1px rgba(0,0,0,0.48);
        -webkit-box-shadow: 1px 3px 5px 1px rgba(0,0,0,0.48);
        -moz-box-shadow: 1px 3px 5px 1px rgba(0,0,0,0.48);
        z-index: 10;
    }

    .nav-item:hover{
        color: var(--ele-blue) !important;
        text-decoration: underline 2px var(--ele-red);
    }
    
</style>