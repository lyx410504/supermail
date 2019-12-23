<template>

  <tab-bar>
    <tab-bar-item link="/home" activeColor="#0c1b99">
      <img slot="tab-icon" src="~/assets/img/tabbar/shou.svg">
      <img slot="tab-icon-active" src="~/assets/img/tabbar/shou1.svg">
      <div slot="tab-text">首页</div>
    </tab-bar-item>
    <tab-bar-item link="/classic" activeColor="#0c1b99">
      <img slot="tab-icon" src="~/assets/img/tabbar/class.svg">
      <img slot="tab-icon-active" src="~/assets/img/tabbar/class1.svg">
      <div slot="tab-text">分类</div>
    </tab-bar-item>
    <tab-bar-item link="/cart" activeColor="#0c1b99">
      <img slot="tab-icon" src="~/assets/img/tabbar/car.svg">
      <img slot="tab-icon-active" src="~/assets/img/tabbar/car1.svg">
      <div slot="tab-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item link="/profile" activeColor="#0c1b99">
      <img slot="tab-icon" src="~/assets/img/tabbar/my.svg">
      <img slot="tab-icon-active" src="~/assets/img/tabbar/my1.svg">
      <div slot="tab-text">我的</div>
    </tab-bar-item>
  </tab-bar>

</template>

<script>
  import TabBar from 'components/common/tabbar/TabBar'
  import TabBarItem from 'components/common/tabbar/TabBarItem'
  export default{
    name:'MainTabBar',
    components: {
      TabBar,
      TabBarItem
    }
  }
</script>

<style>
</style>
