
<div class="container" id="contact">
    <h1 class="red word-1 text-center mb-4 title">Contáctenos</h1>

    <div class="row">
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="exampleFormControlInput1">Nombre:</label>
                <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com">
              </div>
        </div>
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="exampleFormControlInput1">Teléfono:</label>
                <input type="number" class="form-control" id="exampleFormControlInput1">
            </div>
        </div>
        <div class="col-12 col-lg-4">
            <div class="form-group">
                <label for="exampleFormControlInput1">Asunto:</label>
                <input type="email" class="form-control" id="exampleFormControlInput1">
              </div>
        </div>

        <div class="col-12 mt-3">
            <div class="form-group">
                <label for="exampleFormControlTextarea1">Mensaje:</label>
                <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
              </div>
        </div>

        <div class="col-12 mt-3 d-flex">
            <h3 class="red mb-0"> O contáctanos a través de nuestras Redes Sociales:</h3>
            <div class="social-media">
                <a href="https://www.youtube.com/channel/UCnyCs_DgCcPrjRRcLB9KX0A" target="_blank">
                    <img src="/src/assets/YT.png" alt="">
                </a>
                <a href="https://wa.me/51940294166" target="_blank">
                    <img src="/src/assets/Wsp.png" alt="">
                </a>
                <!--<a href="https://www.instagram.com/eleomartt/" target="_blank">
                    <img src="/src/assets/Ig.png" alt="">
                </a>-->
                <!--<a>
                    <img src="/src/assets/TikTok.png" alt="">
                </a>-->
                <a href="https://www.facebook.com/Eleomartt" target="_blank">
                    <img src="/src/assets/Facebook.png" alt="">
                </a>
            </div>
        </div>

        <div class="col-12 d-flex justify-content-center mt-3">
            <button class="btn btn-ele">Enviar</button>
        </div>
    </div>
</div>


<style>

    .social-media{
        display: flex;
        align-items: center;
    }
    .social-media img{
        margin: 5px 10px 10px 10px;
        width: 25px;
        height: 25px;
    }
    #contact{
        padding: 100px 0;
    }

    .title{
        font-weight: bold;
        text-shadow: 2px 2px 0px var(--ele-blue);
    }

    .btn-ele{
        background-color: var(--ele-blue);
        color: white;
    }
</style>
