<template>
  <div>
    <div class="position">
      <span class="iconfont position__icon">&#xe7f1;</span>
      <span class="postion__location">罗德岛</span>
      <span class="position__notice iconfont ">&#xe718;</span>
    </div>

    <div class="search">
      <span class="iconfont">&#xe755;</span>
      <span class="search__text">商店优惠物品</span>
    </div>
    <div class="banner"><img class="banner__img" src="http://www.dell-lee.com/imgs/vue3/banner.jpg" alt="" /></div>
    <div class="icons">
      <div class="icons__item" v-for="item in iconsList" :key="item.imgName">
        <img class="icons__item__img" :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`" />
        <p class="icons__item__desc">{{item.desc}}</p>
      </div>

    </div>
    <div class="gap"></div>
  </div>
</template>

<script>

export default {
  name: 'StaticPart',
  data () {
    return {
      iconsList: [
        { imgName: '超市', desc: '超市便利' },
        { imgName: '菜市场', desc: '菜市场' },
        { imgName: '水果店', desc: '水果店' },
        { imgName: '鲜花', desc: '鲜花绿植' },
        { imgName: '医药健康', desc: '医药健康' },
        { imgName: '家居', desc: '家居时尚' },
        { imgName: '蛋糕', desc: '烘焙蛋糕' },
        { imgName: '签到', desc: '签到' },
        { imgName: '大牌免运', desc: '大牌免运' },
        { imgName: '红包', desc: '红包套餐' },

      ]
    }
  },
}
</script>

<style scoped lang="scss">
@import "../../style/variables.scss";
@import "../../style/mixins.scss";

.position {
  position: relative;
  padding: 0.16rem 0;
  height: 0.22rem;
  line-height: 0.22rem;
  font-size: 0.16rem;
  color: $content-fontColor;
  &__location {
    @include ellipsis;
  }
  & &__icon {
    // position: absolute;
    margin-right: 0.08rem;
    font-size: 0.2rem;
  }
  & &__notice {
    position: absolute;
    right: 0;
    font-size: 0.2rem;
  }
}
.search {
  height: 0.32rem;
  margin-bottom: 0.12rem;
  color: #b7b7b7;
  font-size: 0.16rem;
  line-height: 0.32rem;
  border-radius: 0.16rem;
  background-color: $content-bgColor;
  overflow: hidden;

  .iconfont {
    position: absolute;
    display: inline-block;
    margin: 0 0.1rem 0 0.16rem;
    font-size: 0.2rem;
  }
  &__text {
    margin-left: 0.44rem;
  }
}

.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}
.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0 0.06rem 0;
      text-align: center;
      color: $content-fontColor;
      line-height: 0.17rem;
    }
  }
}
.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background-color: $content-bgColor;
}
</style>
