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
</template>

<style scoped>
header {
  line-height: 1.5;
}

.wrapper{
}

main{
}
</style>
