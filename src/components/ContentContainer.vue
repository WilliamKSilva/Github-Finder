<template>
  <div id="content">
    <section>
      <input 
        type="text"
      />  
    </section>
  </div>
</template> 

<script>
export default {
  name: 'ContentContainer',  
}
</script>

<style scoped>
  #content {
    display: flex;
    
    margin-bottom: 10px;
    padding: 2rem 1rem 2rem;
    background-color: #003459;
  }
</style>