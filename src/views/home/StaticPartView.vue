<template>
  <div class="position">
    <span class="iconfont position__icon">&#xe7f1;</span>
    北京理工大学国防科技园2号楼10层
    <span class="iconfont position__bell">&#xe7c4;</span>
  </div>
  <div class="search">
    <span class="iconfont">&#xe6ac;</span>
    <span class="search__text">山姆会员商店优惠产品</span>
  </div>
  <div class="banner">
    <img
      class="banner__img"
      src="http://www.dell-lee.com/imgs/vue3/banner.jpg"
    />
  </div>
  <div class="icons">
    <div class="icons__item" v-for="item in staticPartList" :key="item.id">
      <img
        class="icons__item__img"
        :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`"
      />
      <p class="icons__item__desc">{{ item.text }}</p>
    </div>
  </div>
  <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart',
  setup() {
    const staticPartList = [
      {
        id: 1,
        imgName: '超市',
        text: '超市便利',
      },
      {
        id: 2,
        imgName: '菜市场',
        text: '菜市场',
      },
      {
        id: 3,
        imgName: '水果店',
        text: '水果店',
      },
      {
        id: 4,
        imgName: '鲜花',
        text: '鲜花绿植',
      },
      {
        id: 5,
        imgName: '医药健康',
        text: '医药健康',
      },
      {
        id: 6,
        imgName: '家居',
        text: '家居时尚',
      },
      {
        id: 7,
        imgName: '蛋糕',
        text: '烘培蛋糕',
      },
      {
        id: 8,
        imgName: '签到',
        text: '签到',
      },
      {
        id: 9,
        imgName: '大牌免运',
        text: '大牌免运',
      },
      {
        id: 10,
        imgName: '红包',
        text: '红包套餐',
      },
    ]
    return { staticPartList }
  },
}
</script>

<style lang="scss" scoped>
@import '../../style/variables.scss';
@import '../../style/mixins.scss';
.position {
  position: relative;
  padding: 0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position__bell {
    position: absolute;
    right: 0;
    top: 0.17rem;
    font-size: 0.2rem;
  }
  color: $content-fontColor;
}
.search {
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background-color: #f5f5f5;
  color: #b7b7b7;
  border-radius: 0.16rem;
  font-size: 0.14rem;
  .iconfont {
    padding: 0 0.08rem 0 0.16rem;
    display: inline-block;
    font-size: 0.14rem;
  }
  &__text {
    display: inline-block;
    font-size: 0.14rem;
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
      text-align: center;
      margin: 0.06rem 0 0.16rem 0;
      color: $content-fontColor;
    }
  }
}
.gap {
  height: 0.1rem;
  background-color: $content-bgColor;
  margin: 0 -0.18rem;
}
</style>
