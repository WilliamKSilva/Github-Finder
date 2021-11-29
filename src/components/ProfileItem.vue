<template>
  <div class="content">
    <div class="main">
      <span>{{title}}</span>
      <p>{{content}}</p>
    </div>
  </div>
</template> 

<script>

export default {
  name: 'ProfileItem', 
  props: {
    title: String, 
    content: String,
    user: String
  }, 
}
</script>

<style scoped>
  .content {
    width: 100%;
  }

  .main {
    display: flex;
    
    justify-content: flex-start;
    align-items: center;
    flex-direction: row;
    
    padding: 2rem 2rem 0;
  }

  .main > span {
    
    padding: 0 0.5rem 0;
  }
  
</style>
