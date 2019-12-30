<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import util from '@/libs/util'
export default {
  name: 'app',
  watch: {
    '$i18n.locale': 'i18nHandle'
  },
  created () {
    this.i18nHandle(this.$i18n.locale)
  },
  methods: {
    i18nHandle (val, oldVal) {
      util.cookies.set('lang', val)
      document.querySelector('html').setAttribute('lang', val)
    }
  }
}
</script>

<style lang="scss">
@import '~@/assets/style/public-class.scss';
#app
  .d2-layout-header-aside-group{
    background-image: url('./views/images/img/bjss.png') !important;
  }
  .el-menu-item.is-active{
    color:aqua !important; 
    font-weight: 800 !important;
    background-image: url('./views/images/img/xuanzhong.png') !important;
    background-position: center bottom !important;
    background-repeat: no-repeat;
  }
  .el-menu-item{
    color:aqua !important; 
    text-align: center !important;
  }
  .el-submenu__title{
   color:aqua !important; 
  }
  .el-tabs__item{
    color:aqua !important;
  }
  .el-icon-arrow-down:before{
     color:aqua !important;
  }
  .el-tabs--card>.el-tabs__header .el-tabs__item{
    border-bottom: 1px solid transparent !important; 
   border-left: 1px solid transparent !important;
  }
  .el-tabs--card>.el-tabs__header .el-tabs__nav{
    border: none !important;
  }
  .fa-navicon:before, .fa-reorder:before, .fa-bars:before{
    color:aqua !important;
  }
  .fa-home:before{
     color:aqua !important;
  }
  .fa-sliders:before{
     color:aqua !important;
  }
  .fa-edit:before, .fa-pencil-square-o:before{
    color:aqua !important;
  }.fa-group:before, .fa-users:before{
    color:aqua !important;
  }
  .fa-tv:before, .fa-television:before{
     color:aqua !important;
  }
  .fa-wrench:before{
     color:aqua !important;
  }
  .fa-bar-chart-o:before, .fa-bar-chart:before{
     color:aqua !important;
  }
  .fa-file-text:before{
    color:aqua !important;
  }
  .fa-pie-chart:before{
   color:aqua !important;
  }
  .fa-map:before{
    color:aqua !important;
  }
  .fa-cubes:before{
    color:aqua !important;
  }
  .d2-layout-header-aside-group .d2-layout-header-aside-content .d2-theme-header{
    background: rgba(0,0,0,0.3) !important;
  }
  .d2-layout-header-aside-group .d2-layout-header-aside-content .d2-theme-container .d2-theme-container-main .d2-theme-container-main-header{
    display: none !important;
  }
  .d2-layout-header-aside-group .d2-layout-header-aside-content .d2-theme-container .d2-theme-container-main .d2-theme-container-main-body .container-component .d2-container-full .d2-container-full__body{
    overflow: hidden;
    overflow-y: scroll;
    margin-right: -20px;
  }
  .d2-layout-header-aside-group .d2-layout-header-aside-content .d2-theme-header .el-menu .el-menu-item{
    display: none;
  }
</style>
