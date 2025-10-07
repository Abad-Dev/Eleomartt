<script>
    import Conact from "../assets/images/muvum_contact.jpg"
</script>
<div class="container">
    <div class="position-relative  mb-5"  id="contactenos">
        <img src={Conact} alt="..." class="w-100" style="height: 270px; object-fit: cover; border-radius: 10px;">
        
        <div class="text-overlay" style=" border-radius: 10px;">
            <h5 class="text-white text-center"><i>Lleva tu operación logística al </i></h5>
            <h1 class="red word-1 my-3 text-center">siguiente nivel</h1>
            <h3 class="text-white mt-2 text-center">con <strong style="color: #1AA7E0; background-color: #f5863450;">&nbsp;Muvum&nbsp;</strong> en Perú</h3>
        </div>
    </div>
    <!-- <h1 class="red word-1 text-center mb-4 title">Contáctenos</h1> -->
    <div class="row">
        <div class="col-12 col-md-6">
            <h3 class="blue">Información de Contacto:</h3>
            <ul class="contact-list">
                <li>
                    <i class="bi bi-geo-alt-fill"></i>
                    <strong class="red">Oficina: </strong>
                    Calle Los Planetas Mz L lote 13 Asc. Fortaleza Ate Vitarte, Lima - Perú
                </li>
                <li>
                    <i class="bi bi-telephone-fill"></i>
                    <strong class="red">Nro. de Celular: </strong>
                    +51 989654193
                </li>
                <li>
                    <i class="bi bi-envelope-fill"></i>
                    <strong class="red">Correo Electrónico: </strong>
                    jalvaradot@jecaudservis.com
                </li>
            </ul>
        </div>
        <form class="col-12 col-md-6" action="https://formsubmit.co/jalvaradot@jecaudservis.com" method="POST">
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
</div>


<style>
    .contact-list {
        display: flex;
        flex-direction: column;
        list-style: none;
        padding: 0;
        font-size: 18px;
        font-weight: 600;
        margin-top: 20px;
        gap: 15px;
        padding-left: 20px;
    }

    .contact-list li i{
        color: var(--ele-red);
    }
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
