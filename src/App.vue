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

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  @media (max-widhth: 1080px) {
    font-size: 93.75%;
  }
  @media (max-widhth: 720px) {
    font-size: 87.5%;
  }
}
body {
  background: #00171f;
  -webkit-font-smoothing: antialised;
}
body, input, textarea, button {
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
}
h1, h2, h3, h4, h5, h6, strong {
  font-weight: 600;
}
button {
  cursor: pointer;
}
[disabled] {
  opacity: 0.6;
  cursor: not-allowed;
}

main {
  display: flex;
  margin-top: 8rem;
}

main {
  display: flex;
  margin-top: 8rem;
}

</style>
