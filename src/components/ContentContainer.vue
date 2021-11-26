<template>
  <div class="content">
    <section>
      <h1>
        Pesquise o perfil!
      </h1>
      <input 
        type="text"
      />  
      <button>
        Pesquisar
      </button>
    </section>
  </div>
</template> 

<script>
export default {
  name: 'ContentContainer',  
}
</script>

<style scoped>
  .fa {
    color: #FFFFFF;
    font-size: 10px;
  }
  
  .content {
    display: flex;
        
    padding: 2rem 1rem 2rem;
    background-color: #003459;

    margin: 0 auto;
  }

  section {
    display: flex;
    align-items: center;
    flex-direction: row;
  }
  
  h1 {
    font-size: 15px;

    padding-right: 10px;
  }

  input {
    cursor: pointer;
    color: #00171f;
    border: 2px solid #FFFFFF;
    transition: 180ms box-shadow ease-in-out;
  }

  input:focus {
    box-shadow: 0 0 0 3px #007ea7;
    outline: 3px solid transparent;
  }

  button {    
    border: 0;
    border-radius: 3px;
    
    height: 100%;
    padding: 4.5px 6px;
    margin-left: 10px;
    
    text-decoration: none;
    text-align: center;
    
    background-color: #FFFFFF;
    color: #00171f;
    
    transition: 0.2s;
  }

  button:hover {
    filter: brightness(0.5);
  }

</style>
