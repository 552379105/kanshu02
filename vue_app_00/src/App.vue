<!--App.vue-->
<template>
 <div class="app-container">
    <!--1:顶部导航栏-->
   
    <!--2:router-view-->
    <router-view>
    </router-view>
    <!--3:tabbar-->
    <nav class="mui-bar mui-bar-tab">
          <router-link to="/Bookshelf" class="mui-tab-item mui-active" href="#tabbar">
            <span class="mui-icon-extra mui-icon-extra-xiaoshuo"></span>
            <span class="mui-tab-label">书架</span>
          </router-link>
          <router-link to="/Home" class="mui-tab-item" href="#tabbar">
            <span class="mui-icon-extra mui-icon-extra-find"></span>
            <span class="mui-tab-label">发现</span>
          </router-link>
          <router-link to="/ShopList" class="mui-tab-item" href="#tabbar">
            <span class="mui-icon mui-icon-extra mui-icon-extra-order">
            <!-- {{$store.getters.opCartCount}} -->
            <span class="mui-badge">1</span>
            </span>
            <span class="mui-tab-label">分类</span>
          </router-link>
        <router-link to="/Base" class="mui-tab-item" href="#tabbar">
            <span class="mui-icon mui-icon-person"></span>
            <span class="mui-tab-label">
            我的</span>
        
        </router-link>
		</nav>
 </div>
</template>

<style>
/*App.vue 顶部和底部导航栏*/
*{margin:0px;
padding:0px;}
.app-container .mint-search {
 height:60px;
}
.app-container{
   padding-bottom:50px;
   overflow-x:hidden;
   position:relative;
}

 .mui-bar-tab .mui-active .mui-tab-label{
    color: #007aff;
 }
.mui-bar-tab .mui-tab-item-tao {
    display: table-cell;
    overflow: hidden;
    width: 1%;
    height: 50px;
    text-align: center;
    vertical-align: middle;
    white-space: nowrap;
    text-overflow: ellipsis;
    color: #929292;
}
.mui-bar-tab .mui-tab-item-tao .mui-icon {
    top: 3px;
    width: 24px;
    height: 24px;
    padding-top: 0;
    padding-bottom: 0;
}
.mui-tab-label{
  font-size:11px;
  display:block;
}
.mui-bar-tab .mui-tab-item-tao .mui-tab-label {
   font-size:11px;
   display:block;
   overflow:hidden;
   text-overflow:ellipsis;

}

</style>
