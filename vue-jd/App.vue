<template>
  <div id="app"> 
    <div class="butt">
      <router-link class="couter" to="/">
      <!-- Home -->
      <!-- <img src="./assets/首页.svg" alt=""> -->
      <i class="el-icon-s-home"></i>
      <span>首页</span></router-link>
      <router-link class="couter" to="/about"><i class="el-icon-s-unfold"></i>
      <span>搜索</span></router-link>
      <router-link class="couter" to="/chat"><i class="el-icon-shopping-cart-2"></i>
      <span>购物车</span></router-link>
      <router-link class="couter" to="/geren"><i class="el-icon-user-solid"></i>
      <span>未登录</span></router-link>
     </div> 

     <div class="content">
        <router-view/>
    </div>
    <!--
    <div class="footer">
    <footerr></footerr>
    </div> -->
 
   
  </div>
</template>
<script>
    import footerr from './views/footerr'
      export default {
        name:"app",
        methods:{
        },
        components:{
          'footerr':footerr,
        },
      }
</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0 ;
}
.couter i{
  font-size: 24px;
}
#app{
  display: flex;
  justify-content: space-between;
  text-align: center;
  position: relative;
  bottom: 0;
}
#app a{
  text-decoration: none;
  &.router-link-exact-active {
      color: #e63a24;
    }
}
.butt{
  width: 100%;
  height: 50px;
  position: fixed;
  bottom: 0;
  left: 0;
  display: flex;
}
.couter{
  flex: 1;
  justify-content: center;
  align-items: center;
  color: #000000;
  display: flex;
  flex-direction:column; 
}
.couter span{
  font-size: 12px;
}
</style>
