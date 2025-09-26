<script>
  export let imgSrc = "";
  export let title = "";
  export let subTitle = "";
  export let descripcion = "";
</script>

<div class="card-container">
  <div class="img-container">
    <img src={imgSrc} alt="...">
  </div>
  <div class="text-container">
    <small class="subtitle"><i>{subTitle}</i></small>
    <h4 class="red">{title}</h4>
    <p class="text-secondary">{descripcion}</p>
  </div>
</div>

<style>
  .card-container{ 
    border-radius: 30px;
    height: 550px;
    width: 330px;
    box-shadow: 1px 1px 11px 0px #323232;
    transition-duration: .4s;
    overflow: hidden;
    border: 10px solid var(--ele-red);
  }

  .card-container:hover{
    transform: translateY(-10px);
    box-shadow: 1px 11px 15px 0px #323232;
  } 

  .img-container {
    height: 300px;
    width: 100%;
    overflow: hidden;
    border-bottom: 1px solid gray;
  }

  .img-container img {
    width: 100%;
    height: auto;
    max-height: 100%;
    object-fit: cover;
    object-position: center;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    gap: 10px;
    width: 100%; 
    height: 100%;
    padding: 20px;
    text-align: center;
  }

  .subtitle {
    text-transform: uppercase;
    font-size: 10px;
    font-weight: bolder !important;
  }
</style>