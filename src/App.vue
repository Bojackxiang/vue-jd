<template>
  <div class="docker">
    <span class="docker__item">
      <i class="el-icon-s-home"> </i>
      <span>首页</span>
    </span>
    <span class="docker__item">
      <i class="el-icon-shopping-cart-2"></i>
      <span>购物车</span>
    </span>
    <span class="docker__item">
      <i class="el-icon-user"></i>
      <span>用户</span>
    </span>
    <span class="docker__item">
      <i class="el-icon-setting docker__item"></i>
      <span>设置</span>
    </span>
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
  i {
    font-size: 0.25rem;
  }
  span {
    display: block;
    font-size: 0.1rem;
    transform: scale(0.8, 0.8);
  }
}
</style>
