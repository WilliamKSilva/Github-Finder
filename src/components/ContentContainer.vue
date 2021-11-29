<template>
  <div class="content">
    <div class="wrapper">
      <section class="header">
        <h1>
          Pesquise o perfil!
        </h1>
        <input 
          type="text" 
          placeholder="Usuário a ser buscado..."
          v-model="url"        
        />  
        <button @click="getUser">
          Pesquisar
        </button>
      </section>
      <div class="main">
        <div class="avatar">
          <img 
            v-bind:src="data.avatar_url || 'https://cdn.iconscout.com/icon/free/png-256/account-avatar-profile-human-man-user-30448.png'" 
            alt="avatar"
            width="100"
          />
        </div> 
        <div class="profileItems">          
          <ProfileItem title="Name:" v-bind:content="data.name" :user="user"/>
          <ProfileItem title="Profile Link:" v-bind:content="data.html_url"/>
          <ProfileItem title="Location:" v-bind:content="data.location"/>
          <ProfileItem title="Company:" v-bind:content="data.company"/>
          <ProfileItem title="Repos:" v-bind:content="data.public_repos"/>
        </div>  
      </div>
    </div>
  </div>
</template> 

<script>
import axios from 'axios'
import ProfileItem from './ProfileItem.vue'

export default {
  name: 'ContentContainer',  
  data() {
    return {
      user: String,
      url: null, 
      data: []
    }
  },
  state: {
    primeiro: null
  },
  components: {
    ProfileItem
  },   
  methods: {
     async getUser() {      
      const response = await axios.get(`https://api.github.com/users/${encodeURIComponent(this.url)}`)
      this.data = response.data;
    }
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
