<script>
  export let imgSrc = "";
  export let title = "";
  export let descripcion = "";
  export let url = "#";
</script>

<div class="card-container mx-2">
  <div class="img-container">
    <img src={imgSrc} alt="...">
  </div>
  <div class="text-container">
    <h4 class="red">{title}</h4>
    <p class="text-secondary my-2">{descripcion}</p>

    <a class="w-100 px-2" href={url} target="_blank">
      <button class="btn-primary justify-content-center w-100">Conocer más</button>
    </a>
  </div>
</div>

<style>
  .card-container{ 
    border-radius: 30px;
    width: 330px;
    box-shadow: 1px 1px 11px 0px #323232;
    transition-duration: .4s;
    overflow: hidden;
  }

  .card-container:hover{
    transform: translateY(-10px);
    box-shadow: 1px 11px 15px 0px #323232;
  } 

  .img-container {
    display: flex;
    align-items: center;
    height: 215px;
    width: 100%;
    overflow: hidden;
    border-bottom: 1px solid gray;
  }

  .img-container img {
    width: 100%;
    height: auto;
    max-height: 100%;
    object-fit: contain;
    object-position: center;
    background-color: lightgray;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    gap: 10px;
    width: 100%; 
    height: 100%;
    padding: 30px;
    text-align: center;
  }
</style>