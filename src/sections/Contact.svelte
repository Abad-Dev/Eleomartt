<script>
    import Operador from "../assets/images/operador.jpg"
</script>
<div class="container">
    <div class="position-relative  mb-5"  id="contactenos">
        <img src={Operador} alt="..." class="w-100" style="height: 270px; object-fit: cover; border-radius: 10px;">
        
        <div class="text-overlay" style=" border-radius: 10px;">
            <h5 class="text-white mb-5 text-center"><i>¿Listo para optimizar tu almacén?</i></h5>
            <h1 class="text-white word-1 text-center">Solicita tu</h1>
            <h1 class="red word-2 text-center">Cotización</h1>
        </div>
    </div>
    <!-- <h1 class="red word-1 text-center mb-4 title">Contáctenos</h1> -->
    <form action="https://formsubmit.co/chuamani@jacaudservice.com" method="POST">
    <div class="row">
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="nombre">Nombre:</label>
                <input type="email" class="form-control" id="nombre" name="nombre" placeholder="nombre@ejemplo.com">
              </div>
        </div>
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="telefono">Teléfono:</label>
                <input type="number" class="form-control" name="telefono" id="telefono">
            </div>
        </div>
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="asunto">Asunto:</label>
                <input type="text" class="form-control" name="asunto" id="asunto">
              </div>
        </div>

        <div class="col-12 mt-3">
            <div class="form-group">
                <label for="mensaje">Mensaje:</label>
                <textarea class="form-control" name="mensaje" id="mensaje" rows="3"></textarea>
              </div>
        </div>

        <div class="col-12 d-flex justify-content-center mt-3">
            <button class="btn-primary">
                Enviar
                <i class="bi bi-send-fill"></i>
            </button>
        </div>
    </div>
    </form>
</div>


<style>
    .text-overlay {
        position: absolute;
        top: 0;
        left: 0;

        background-color: rgba(0, 0, 0, 0.5);
        height: 100%;
        width: 100%;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
</style>
