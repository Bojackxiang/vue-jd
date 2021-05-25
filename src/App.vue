<template>
  <div>
    <div class="wrapper">
      <div class="location">
        <i class="location__icon el-icon-location-outline" />
        <span> this is my location</span>
        <i class="location__icon el-icon-message-solid"></i>
        <div></div>
      </div>
      <el-input
        v-model="searchInput"
        prefix-icon="el-icon-search"
        placeholder="search"
      />
      <div class="banner">
        <img class="banner__img" :src="bannerUrl" alt="" />
      </div>
      <div>hello</div>
    </div>
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
    const searchInput = "";
    const bannerUrl =
      "https://png.pngtree.com/thumb_back/fw800/background/20190506/pngtree-simple-banner-fading-background-image_102822.jpg";
    return {
      dockerItems,
      searchInput,
      bannerUrl,
    };
  },
};
</script>


<style lang="scss">
@import "./styles/config.scss";
@import "./styles/mixins.scss";
.wrapper {
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0.5rem;
  padding: 0 0.18rem;
  .location {
    @include flexCenterAll();
    padding: 0.15rem 0;
    font-size: 0.16rem;
    &__icon {
      margin-top: 0.05rem;
      font-size: 0.25rem;
      margin-right: 0.1rem;
      line-height: 0.22rem;
    }
    span {
      display: inline-block;
      flex: 1;
    }
  }
  .banner {
    background-color: pink;
    min-height: 1rem;
    &__img {
      width: 100%;
    }
  }
}
.docker {
  position: absolute;
  display: flex;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 0.01rem solid #000;
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
