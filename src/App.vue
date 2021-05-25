<template>
  <div class="docker">
    <span class="docker__item">test</span>
    <span class="docker__item">test</span>
    <span class="docker__item">test</span>
    <span class="docker__item">test</span>
  </div>
</template>

<style lang="scss">
.docker {
  position: absolute;
  display: flex;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 1px solid #000;
  align-items: center;
  justify-content: space-evenly;
}
.docker__item {
  flex: 1;
  text-align: center;
}
</style>
