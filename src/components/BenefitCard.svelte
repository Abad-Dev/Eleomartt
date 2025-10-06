<script>
  export let icon = "";
  export let title = "";
  export let descripcion = "";

  let iconClass = "bi bi-" + icon;
</script>

<div class="card-container">
  <div class="icon-container">
    <div class="icon">
      <i class={iconClass}></i>
    </div>
  </div>

  <div class="text-container">
    <h4 class="red">{title}</h4>
    <p class="text-secondary">{descripcion}</p>
  </div>
</div>

<style>
  .card-container{
    border-radius: 30px;
    width: 330px;
    box-shadow: 0px 0px 10px 0px #32323286;
    transition-duration: .4s;
    overflow: hidden;
    padding: 30px;
  }

  .card-container:hover{
    transform: translateY(-5px);
    box-shadow: 0px 0px 25px 0px var(--ele-red);
  }

  .icon-container{
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .icon {
    width: 120px;
    height: 120px;
    background-color: var(--ele-red);
    color: white;
    border-radius: 100%;
    position: relative;

    display: grid;
    place-items: center;
    font-size: 40px;
  }

  .icon::after {
    content: '';
    width: 23px;
    height: 23px;
    background-color: #1AA7E0;
    border-radius: 50%;
    position: absolute;
    top: 18px;
    right: 18px;
    transform: translate(50%, -50%);
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
</style>