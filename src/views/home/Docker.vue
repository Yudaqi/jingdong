<template>
  <!-- docker start -->

  <div class="docker">
    <div v-for="(item ,index) in dockerList" :class="{'docker__item--active':index ===0} " class="docker__item" :key="item.icon">
      <div class="iconfont" v-html="item.icon"></div>
      <div class="docker__title">{{item.text}}</div>
    </div>
  </div>
  <!-- docker end -->
</template>

<script>
export default {
  name: 'Docker',
  // setup () {
  //   const dockerList = [
  //     { icon: '&#xe630;', text: '首页' },
  //     { icon: '&#xe6af;', text: '购物车' },
  //     { icon: '&#xe713;', text: '订单' },
  //     { icon: '&#xe78b;', text: '我的' }

  //   ]
  //   return { dockerList }
  // }

  data: function () {
    return {
      dockerList: [{ icon: '&#xe630;', text: '首页' },
      { icon: '&#xe6af;', text: '购物车' },
      { icon: '&#xe713;', text: '订单' },
      { icon: '&#xe78b;', text: '我的' }]
    }
  },

}

</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
.docker {
  display: flex;
  box-sizing: border-box;
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  padding: 0 0.18rem;
  border-top: 1px solid #f1f1f1;
  color: $content-fontColor;
  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &--active {
      color: #1fa4fc;
    }
  }
  &__title {
    font-size: 20px;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>
