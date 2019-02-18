<template>
    <div class="app-base">
        <div class="base-top">
            <div class="picture">
              <img src="../../img/person.jpg"alt=""/>
            </div> 
                <div class="base-msg">
                    <h4>游客</h4>
                    <div>金币0</div>
                </div>
                <span class="mui-icon mui-icon-forward"
                  style="padding-left:100px;padding-top:35px;width:100px;float:right;"
                > </span>
            </div>
   <!--读过的书,购买的书-->
    <div class="base-top1">
        <div style="border-right:1px solid #ccc;">
              <div class="book_number"> <h4>8</h4>  本
              </div>
           <span>读过的书</span>
        </div>
        <div>
          <div class="book_number">  <h4>0</h4>章 </div>
           <span>购买的书</span>    
        </div> 
     </div>
    <div class="deliever"></div>
    <!--列表-->
      <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
      <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
      <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
       <div class="deliever"></div>
    <!--列表-->
        <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
        <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
        <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
            <div class="deliever"></div>
    <!--列表-->
         <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
         <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>
        <button type="button" class="mui-btn mui-btn-block mui-btn-outlined"> 
       <span class="mui-icon-extra mui-icon-extra-prech" > </span>
      充值
       <span class="mui-icon mui-icon-forward" style="margin-top:5px;float:right;"> </span>
      </button>


   </div>
</template>
<style>
 .app-base .mui-btn-outlined{
     padding-left:5px;
      text-align:left;
}
.book_number{
   display:flex;
    padding-left:77px;
    line-height:30px;
}
.base-top1{
 width:100%;
 height:60px;
 display:flex;
 text-align:center;
}
.base-top1 div{
    height:70%;
   width:50%;
   text-align:center;
}
.app-base{
    font-size:14px;
    background:#fff; 
    width:100%;
    height:1200px;

   }
 .base-top{
  display:flex;
     width:100%;
     height:150px;
       padding-top:15px;
   padding-left:25px;
 }
 .picture{
   width:100px;
   height:100px;
   overflow:hidden;
   border-radius:50%;
 
 }
 .picture img{
     width:100px;
     height:100px;
 }
 .base-msg{
     margin-top:13px;
     margin-left:21px;
     width:100px;
     height:100%;
     line-height:20px;
 }
</style>
<script>
  import {Toast} from  "mint-ui";
   export default {
      data(){
          return{}
      },
     created(){},
     methods:{}
   }

</script>