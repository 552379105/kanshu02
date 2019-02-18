<template>

    <div class="app-detail" :id="id">
       <!--顶部导航栏-->
       	<header id="header" class="mui-bar mui-bar-nav">
           <router-link to="/Home">
                <a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
            </router-link>
            <!--顶部右边的图表-->    
			<span class="mui-icon-extra mui-icon-extra-share mui-pull-right detail-top-right "></span>
             <span class="mui-icon mui-icon-home-filled mui-pull-right" style="margin-right:30px;"> </span>
            </a>
		    
        </header>

         <div class="app-book-show">
            <img :src="bnfo.book_url" alt=""/>
             <div class="show-right">
                    <div style="font-size:16px;">{{bnfo.name}}</div>
                    <span>作者  {{bnfo.author}}</span>
                    <span>690万字|完结</span>
                     <span>1.4万人读过</span>
                     <span>5金币/千字</span>
              </div>
           </div>      
         <div :class="classA ? 'app-book-detail' : 'app-book-detail2'">
             {{bnfo.title}} {{bnfo.title}}
             {{bnfo.title}}{{bnfo.title}}
            
              <span class="mui-icon mui-icon-arrowdown mui-pull-right"  v-on:click="Change()"> </span>
              </div>
              <div class="line"> </div>
        <div class="book-catalog">
            <span style="color:#000;"> 查看目录</span> 
            <span> 共2985章 </span>
           
            <span class="mui-icon mui-icon-arrowright mui-pull-right"> </span>
             <span style="float:right;">已完结 </span>
         </div> 
        <div class="detail-commont">
        
            <h4 style="float:left;">书评</h4>
             <a href="#modal" style=" display:block; float:right; color:blue; cursor:pointer;" v-on:click="Sclass()"> 写评论 </a>
             <span class="mui-icon mui-icon-compose mui-pull-right" style="color:blue;"> </span>
         
        </div>

			<div id="modal" class="mui-modal" v-bind:class="classOject">
                <div class="CommontStar">          
                  <span> 评论</span>         
                </div>
			   <div> </div>
             <textarea name="" id="" placeholder="点评这本书..." style="width:100%; height:35%;">
             
             </textarea>
             <div class="commonBottom">
                <img src="../../img/timg.jpg" v-on:click="CloseCommon() ">
                <button> 发送</button>
             </div> 
			</div>
          

    </div>
    
    </template>
    <style>
     .commonBottom {
         width:100%;
         height:60px;
         display:flex;
         justify-content:space-between;
         background-color:rgb(247,247,247);
     }
     .commonBottom img{
        width:30px;
        height:30px;
        margin-left:10px;
        margin-top:10px;
     }
     .commonBottom button{
          width:120px;
          height:42px;
          margin-right:10px;
          margin-top:10px;
          font-size:15px;
     }
    .mui-modal {
    top:336px !important;
 
    }
   .detail-commont{
   width:100%; 
   height:50px;
   }
    .book-catalog{
        margin-top:20px;
        padding-left:10px;
         width:100%;
         height:50px;
         font-size:14px;
         color:#acacac;
        }
         .book-catalog span{
             margin-right:10px;
         }
    .app-book-detail{
        position:relative;
        font-size:15px;
      width:85%;
    margin-left:20px;
    margin-top:20px;
      height:40px;
      overflow:hidden; 
        white-space: nowrap;
       text-overflow:ellipsis; 
    }
    .app-book-detail2{
    position:relative;
        font-size:15px;
      width:85%;
    margin-left:20px;
    margin-top:20px;
      height:150px;
    }
    .line{
            margin-left: 20px;
        width:85%;
        height:0px;
        border-bottom:1px solid #ccc;
    }
.mui-bar{
    background-color:#efebeb !important;
}
 .app-book-show{
     margin-top:44px;
    width:100%;
    height:210px;
    background-color:#efebeb;
    display:flex;
    padding-left:50px;
    padding-top:30px;
 }
 .app-book-show img{
     width:115px;
     height:155px;
 }
 .show-right{
     margin-left:20px;
     font-size:12px;
 }
 .show-right span{
     display:block;
     margin-top:2px;
 }
    *{margin:0;padding:0;}
   .detail-top-right{
       margin-top:10px;
       color:#007aff;
   }
   .app-detail{
       width:100%;
       height:1200px;
       background:#fff;
   }

</style>
<script> 
 import {Toast} from  "mint-ui";
    export default{ 
         props:["id"], 
         created(){
              this.getBooksInfo();
              this.getMore();
         },
        
         data(){    
         return{
                classA:true,
                classOject:"",
                 fb:true,
                  msg:"",
                pageIndex:0,   //当前页码
                pageSize:7,    //页大小
                pageCount:1,   //总页数
                list:[],        //当前页内容
                bnfo:{},
           id:this.$route.query.id
             }
         },
         methods:{   
              Change(){
                //当点击时判断此时的详情介绍的状态,如果是开则关,如果是关则开;
                console.log(this.classA);
                if(this.classA==true){
                  this.classA=false;
                  console.log(this.classA);
                    }else if(this.classA==false){
                        this.classA=true;
                        console.log(this.classA);
                    } 
                },

             Sclass(){
                 //点击时给 id为modal的div添加mui-active变成激活状态
                  if(this.fb==true){
                    this.classOject="mui-active";
                    this.fb=false; 
                  }

             },
           CloseCommon(){
               //当点击叉号的时候关闭评论模态框
                if(this.fb==false){
                    this.classOject="";
                    this.fb=true;
                    }
            },

            getBooksInfo(){

                            //1:获取参数 id
                var id = this.$route.query.id;
                //2:创建变量保存 url地址
                var url = "http://127.0.0.1:3000";
                url +="/getBooksInfo?id="+id;
                //3:发送ajax请求获取数据
                //4:将返回结果保存 info对象
                this.axios.get(url).then(result=>{
                    this.bnfo = result.data.data;
                });

                    }
                    
            },   
        }
    </script>