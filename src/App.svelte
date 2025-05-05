<script>
  let dadoIzquierda = "/dice1.png";
  let dadoDerecha = "/dice1.png";
  let numero1 = 1;
  let numero2 = 2;

  function tirarDados() {
    numero1 = Math.floor(Math.random() * 6) + 1;
    numero2 = Math.floor(Math.random() * 6) + 1;
    dadoIzquierda = '/dice' + numero1 + '.png'
    dadoDerecha = '/dice' + numero2 + '.png'
  }
</script>

<main class="dado">
  <div class="text-center text-bg-secondary h-100 w-100">
    <button class="btn btn-success lg shadow p-3 m-5 rounded" onclick={tirarDados}>Tirar Dados</button>
    <br>
    <img src={dadoIzquierda} alt="Dado 1" class="img">
    <img src={dadoDerecha} alt="Dado 1" class="img">

    {#if numero1 == numero2}
    <h1>
      <span class="badge text-bg-success lg shadow rounded">
        ¡Ganaste!
      </span>
    </h1>
    {/if}
  </div>
</main>

<style>
  .img {
    width: 300px;
    height: 300px;
    background-color: rgba(211, 25, 12, 0.959);
    margin: 30px;
    border-radius: 20px;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px, rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
  }

  .dado{
    height: 100vh;
    
  }
</style>
