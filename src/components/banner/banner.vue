<template> 
  <div class="menu-item" ref = "footer">
    <div class="item">
      <router-link to="/foods">
        <i class="ele" :class="{'active': 2 === footerIndex}"></i>
        <span>外卖</span>
      </router-link>
    </div>
    <div class="item">
      <router-link to="/finds">
        <i class="find" :class="{'active': 1 === footerIndex}"></i>
        <span>发现</span>
      </router-link>
    </div>
    <div class="item">
      <router-link to="/orders">
        <i class="order" :class="{'active': 3 === footerIndex}"></i>
        <span>订单</span>
      </router-link>
    </div>
    <div class="item">
      <router-link to="/myinfo">
        <i class="user" :class="{'active': 4 === footerIndex}"></i>
        <span>我的</span>
      </router-link>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props: ['footerIndex'],
    computed: {
      footerIndex() {
      }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
@import '../../common/stylus/mixin.styl';
.menu-item{
  z-index: 2;
  display: flex;
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: .42rem;
  background: #fff;
}
.menu-item div{
  display: inline-block;
  flex: 1;
  text-align: center;
}
.menu-item div a{
  display: inline-block;
  width: 100%;
  height: 100%;
  color: #666;
}
.menu-item div i,
.menu-item div span{
  display: inline-block;
  vertical-align: top;
  width: 100%;
  text-align: center;
}
.menu-item div i{
  width: .21rem;
  height: .2rem;
  margin-top: .04rem;
}
.menu-item div i.ele{
	background: url(../../common/images/ele.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.find{
	background: url(../../common/images/find.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.order{
	background: url(../../common/images/order.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.user{
	background: url(../../common/images/user.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.ele.active{
	background: url(../../common/images/ele_active.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.find.active{
	background: url(../../common/images/find_active.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.order.active{
	background: url(../../common/images/order_active.png)no-repeat center center;
	background-size: contain;
}
.menu-item div i.user.active{
	background: url(../../common/images/user_active.png)no-repeat center center;
	background-size: contain;
}
.menu-item div span{
  -webkit-transform: scale(.8);
  -moz-transform: scale(.8);
  transform: scale(.8);
}
</style>
