<template>
  <div class="item" :class="reversed ? 'reversed' : ''">
    <div class="container-gradient" v-if="reversed"></div>
    <div class="meta">
      <div>
        <h3>
          <slot name="heading"></slot>
        </h3>
        <div class="info">
          <slot></slot>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default{
  props: ["reversed"]
}
</script>

<style scoped>
.item {
  margin-top: 0;
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 16px;
  border-bottom: 3px solid black;
  min-height: 33vh;
}

.item:not(.reversed){
  background-image: url("pattern_128bw.png");
  background-position: -64px -64px, 0 0;
  animation: animatedBackground 5s linear infinite;
}

.meta {
  flex: 1;
  display: flex;
  justify-content: center;
  z-index: 1;
}

.info{
  max-width: 46rem;
  background-color: rgba(255, 255, 255, 0.75);
  border: 1px solid black;
  padding: 4px;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
  background-color: #434240;
  background: linear-gradient(180deg, #434240, #0f1012);
  color: white;
  border-radius: 6px;
}

.image {
  flex: 1 1 100%;
}

.image img {
  max-width: 100%;
  height: auto;
}

.item.reversed{
  background-color: #a6aaad;
  background-image: url("hmo.jpg");
  background-repeat: no-repeat;
  background-size: cover;

  background-attachment: fixed;
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    /* padding: 0.4rem 0 1rem calc(var(--section-gap) / 2); */
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  /* .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  } */

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }

  .image {
    /* max-width: 50%; */
    flex: 0 0 50%;
    height: auto;
  }

  .item.reversed{
    flex-direction: row-reverse;
  }
}

@keyframes animatedBackground {
    from {
        background-position: -64px -64px, 0 0;
    }

    to {
        background-position: 64px 64px, 128px 128px;
    }
}

.container-gradient{
  background: linear-gradient(180deg, #a6aaad, transparent);
    width: 100%;
    height: 100%;
    position: absolute;
}
.container-gradient::after{
  content: ' ';
}
</style>
