<template>
  <div class="docker">
    <span
      v-for="(item, idx) in dockerItems"
      :key="idx"
      class="docker__item"
      :class="[item.isActive ? 'docker__item--active' : '']"
    >
      <i :class="[item.iconName]"></i>
      <span>{{ item.label }}</span>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    const dockerItems = [
      { iconName: "el-icon-s-home", label: "首页", isActive: true },
      { iconName: "el-icon-shopping-cart-2", label: "购物车" },
      { iconName: "el-icon-user", label: "用户" },
      { iconName: "el-icon-setting", label: "设置" },
    ];
    return {
      dockerItems,
    };
  },
};
</script>


<style lang="scss">
@import "./styles/config.scss";
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
  // & == .docker: 所以这边可以代替
  &__item {
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
  &__item--active {
    color: $color_docker_active_item;
  }
}
</style>
