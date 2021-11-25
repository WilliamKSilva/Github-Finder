<template>
  <header>
    <h1>
      Github-Finder
    </h1>
  </header>
</template> 

<script>
export default {
  name: 'Header',  
}
</script>

<style scoped>
  header {
    display: flex;    
    
    max-width: 1120px;
    margin: 0 auto;
    border-radius: 8px;

    padding: 2rem 1rem 2rem;
    justify-content: center;
    background-color: #003459;
  }
  header > h1 {
    font-size: 25px;    
  }
</style>