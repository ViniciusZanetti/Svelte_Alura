<script lang="ts">
  import Titulo from "./components/Titulo.svelte";

  function aoSubmeter() {
    console.log("Submetido");
  }
</script>

<div class="app">
  <header>
    <h1 class="titulo">Svelte Perfis</h1>
    <Titulo />

    <div class="busca-usuario">
      <form on:submit|preventDefault={aoSubmeter}>
        <input type="text" class="input" />

        <div class="botao-container">
          <button type="submit" class="botao">buscar</button>
        </div>
      </form>
    </div>
  </header>
</div>

<style>
  .app {
    max-height: 100vh;
  }

  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .busca-usuario {
    position: relative;
    width: 70%;
  }

  .titulo {
    font-family: "Roboto";
    font-style: normal;
    font-weight: 800;
    font-size: 38px;
    line-height: 45px;

    color: #3680f4;
    background-image: linear-gradient(to left, #3680f4, #c14fac);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .botao {
    padding: 15px 24px;
    border-radius: 8px;
    border: none;
    background: #2e80fa;
    line-height: 26px;
    color: #fff;
    font-size: 22px;
    cursor: pointer;
  }

  .botao:hover {
    background: #4590ff;
  }

  .botao-container {
    position: absolute;
    width: 9.625rem;
  }

  .input {
    width: calc(100% - 8.75px);
    height: 3.125rem;
    border-radius: 8px;
    border: 1px solid #2e80fa;
    box-shadow: 0px 17px 52px rgba(222, 231, 247, 0.4);
    background: #f5f5f5;
    padding: 15px 25px;
    font-size: 1rem;
    line-height: 26px;
    outline: 0;
  }

  .input::placeholder {
    font-family: "Roboto";
    font-style: italic;
    font-weight: 300;
    font-size: 19.5px;
    line-height: 26px;
    color: #6e8cba;
  }
</style>
