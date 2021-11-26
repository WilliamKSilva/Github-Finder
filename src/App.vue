<template>
  <div id="container">
    <section id="header">
      <Header />
    </section>   
    <main>
      <ContentContainer />
    </main>     
  </div>  
</template>

<script>
import Header from './components/Header'
import ContentContainer from './components/ContentContainer.vue'

export default {
  name: 'App',
  components: {
    Header, 
    ContentContainer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
}
body {
  background-color: #00171f;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

main {
  display: flex;
  margin-top: 8rem;
}

</style>
