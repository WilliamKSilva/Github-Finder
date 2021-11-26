<template>
  <div class="content">
    <div class="wrapper">
      <section class="header">
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
      <div class="main">
        <div class="avatar">
          <img 
            src="https://avatars.githubusercontent.com/u/75429175?v=4" 
            alt="avatar"
            width="100"
          />
        </div> 
        <div class="profileItems">          
          <ProfileItem title="Name:" content="William Kelvin"/>
          <ProfileItem title="Profile Link:" content="https://github.com/WilliamKSilva"/>
          <ProfileItem title="Location:" content="São José dos Campos"/>
          <ProfileItem title="Company:" content="Dataside"/>
          <ProfileItem title="Repos:" content="15"/>
        </div>  
      </div>
    </div>
  </div>
</template> 

<script>
import ProfileItem from './ProfileItem.vue'

export default {
  name: 'ContentContainer',  
  components: {
    ProfileItem
  }
}
</script>

<style scoped>
  .content {
    margin: 0 auto; 

    background-color: #00171f;
  }

  .wrapper {
    border: 2px solid #003459;
    border-radius: 5px;
    
    padding: 2rem 4rem 2rem;
  }
    
  .header {
    display: flex;
    
    width: 100%;
    align-items: center;
    flex-direction: row;
  }
  
  .header > h1 {
    font-size: 15px;

    padding-right: 10px;
  }

  .header > input {    
    color: #00171f;
    border: 2px solid #FFFFFF;
    transition: 180ms box-shadow ease-in-out;
  }

   .header > input:focus {
    box-shadow: 0 0 0 3px #007ea7;
    outline: 3px solid transparent;
  }

   .header > button {    
    border: 0;
    border-radius: 3px;
    
    padding: 4.5px 6px;
    margin-left: 10px;
    
    text-decoration: none;
    text-align: center;
    
    background-color: #FFFFFF;
    color: #00171f;
    
    transition: 0.2s;
  }

   .header > button:hover {
    cursor: pointer;
    filter: brightness(0.5);
  }

  .main {
    display: flex;         
    width: 100%;   
    
    padding: 5rem 2rem 2rem;
  }  

</style>
