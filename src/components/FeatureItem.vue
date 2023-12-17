<template>
  <div class="item" :class="theme ? ['themed', 'theme-' + theme] : ''">
    <slot name="pre-item"></slot>
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
  props: ["reversed", "theme"]
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

.item.theme-skills{
  background-image: url("pattern_128bw.png");
  background-position: -64px -64px, 0 0;
  animation: animatedBackground 5s linear infinite;

  background-attachment: fixed;
}

.meta {
  flex: 1;
  display: flex;
  justify-content: center;
  z-index: 1;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}


.image {
  flex: 1 1 100%;
}

.image img {
  max-width: 100%;
  height: auto;
}

.item.theme-hmo{
  background-color: #a6aaad;
  background-image: url("hmo.jpg");
  background-repeat: no-repeat;
  background-size: cover;

  background-attachment: fixed;
}

.item.theme-showcase{
  background: #8e9eab;  /* fallback for old browsers */
  background: rgb(238,242,243);
  background: radial-gradient(circle, rgba(238,242,243,1) 50%, rgba(142,158,171,1) 100%);
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

  .item.theme-hmo{
    min-height: 50vh;
  }
}

@media (max-width: 1023px) {
  .item{
    min-height: 100vh;
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
</style>
