<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheFeatures from './components/TheFeatures.vue'
import TheHeader from './components/TheHeader.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <TheHeader/>
    </div>
  </header>

  <main>
    <TheFeatures />
  </main>

  <footer>
    <div>
      <p>Hermosillo photo provided by <a href="https://es.wikipedia.org/wiki/Archivo:Vista_HMO.jpg">Wikipedia</a></p>
      <p>Icons provided by <a href="https://iconmonstr.com/">iconmonstr</a></p>
      <p></p>
    </div>
  </footer>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.wrapper{
}

main{
}

footer{
  background-color: #111111;
  color: white;
  padding: 8px;
}
</style>
