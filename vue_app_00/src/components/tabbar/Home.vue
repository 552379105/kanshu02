<template>
  <div class="app-home">
     <!--第一个 学子商城-->
        <mt-search fixed>   </mt-search>
     <!--第二个：轮播图-->
     <mt-swipe :auto="2500">
        <mt-swipe-item v-for="item in list" :key="item.id">
            <img :src="item.img_url" />
        </mt-swipe-item>
     </mt-swipe>
     <!--第三个：九宫格-->
      <ul class="mui-table-view mui-grid-view mui-grid-9">
		      <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
              <router-link to="/Rank">
	              	<img src="../../img/menu1.png" />
		            <div class="mui-media-body">
                 排行</div>
                 </router-link>
                </li>
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
                <router-link to="/GoodsList">
                        <img src="../../img/menu2.png" />
		                    <div class="mui-media-body">
                       完本</div></router-link></li>
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><router-link to="/NewsList">
		                    <img src="../../img/menu3.png" />
		                    <div class="mui-media-body">
                        免费</div></router-link></li>
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
		                    <img src="../../img/menu4.png" />
		                    <div class="mui-media-body">
                        新书</div></a></li>
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3"><a href="#">
		                     <img src="../../img/menu5.png" />
		                    <div class="mui-media-body">会员</div></a></li>
		        </ul>
            <div class="deliever"></div>
         <div class="part1">       
                <div class="zbtj">
                  <h4>主编推荐</h4>
                <a href="#">查看全部</a> 
                </div>  
               <div class=" top1">
                       <ul class="p1">
                         <li>
                         <img src="../../img/p1.jpg"/>
                           <div>神道至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p2.jpg"/>
                          <div>生死至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p3.jpg"/>
                          <div>狂暴皇帝</div>
                         </li>
                       </ul>
                      <ul class="p2" >
                        <li class="book_1" v-for="tmp of mylist" :key="tmp.id">
                        <router-link :to="'/Detail?id='+tmp.id">
                          <img :src="tmp.book_url"/>
                            <div class="book_right">
                                <div>{{tmp.name}}</div>
                                <p>{{tmp.title}} </p>
                                <p>{{tmp.author}}</p>
                            
                            </div>
                            	</router-link>
                        </li>
                      </ul>
                    <div class="deliever"></div>

                </div>  

          </div>
       <div class="part1">       
                <div class="zbtj">
                  <h4>主编推荐</h4>
                <a href="#">查看全部</a> 
                </div>  
               <div class=" top1">
                       <ul class="p1">
                         <li>
                         <img src="../../img/p1.jpg"/>
                           <div>神道至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p2.jpg"/>
                          <div>生死至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p3.jpg"/>
                          <div>狂暴皇帝</div>
                         </li>
                       </ul>
                      <ul class="p2" >
                        <li class="book_1" v-for="tmp of mylist" :key="tmp.id">
                        <router-link :to="'/Detail?id='+tmp.id">
                          <img :src="tmp.book_url"/>
                            <div class="book_right">
                                <div>{{tmp.name}}</div>
                                <p>{{tmp.title}} </p>
                                <p>{{tmp.author}}</p>
                            
                            </div>
                            	</router-link>
                        </li>
                      </ul>
                    <div class="deliever"></div>

                </div>  

          </div>
          <div class="part1">       
                <div class="zbtj">
                  <h4>主编推荐</h4>
                <a href="#">查看全部</a> 
                </div>  
               <div class=" top1">
                       <ul class="p1">
                         <li>
                         <img src="../../img/p1.jpg"/>
                           <div>神道至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p2.jpg"/>
                          <div>生死至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p3.jpg"/>
                          <div>狂暴皇帝</div>
                         </li>
                       </ul>
                      <ul class="p2" >
                       <li class="book_1" v-for="tmp of mylist" :key="tmp.id">
                        <router-link :to="'/Detail?id='+tmp.id">
                          <img :src="tmp.book_url"/>
                            <div class="book_right">
                                <div>{{tmp.name}}</div>
                                <p>{{tmp.title}} </p>
                                <p>{{tmp.author}}</p>
                            
                            </div>
                            	</router-link>
                        </li>
                      </ul>
                    <div class="deliever"></div>

                </div>  

          </div>
          <div class="part1">       
                <div class="zbtj">
                  <h4>主编推荐</h4>
                <a href="#">查看全部</a> 
                </div>  
               <div class=" top1">
                       <ul class="p1">
                         <li>
                         <img src="../../img/p1.jpg"/>
                           <div>神道至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p2.jpg"/>
                          <div>生死至尊 </div>
                         </li>
                         <li>
                         <img src="../../img/p3.jpg"/>
                          <div>狂暴皇帝</div>
                         </li>
                       </ul>
                      <ul class="p2" >
                        <li class="book_1" v-for="tmp of mylist" :key="tmp.id">
                        <router-link :to="'/Detail?id='+tmp.id">
                          <img :src="tmp.book_url"/>
                            <div class="book_right">
                                <div>{{tmp.name}}</div>
                                <p>{{tmp.title}} </p>
                                <p>{{tmp.author}}</p>
                            
                            </div>
                            	</router-link>
                        </li>
                      </ul>
                    <div class="deliever"></div>

                </div>  

          </div>
          
    
     <!--第四个：底部导航栏tabbar-->


  </div>  
</template>
    <script>
    export default {
      data(){
       return {
         mylist:{},
         list:{},     //返回数据
       } 
     },
      created() {
          //当组件对象创建成功后即可发送ajax请求
          this.getImages();
          //获取图书信息
          this.getBook();
      },
      methods:{
         getBook(){
          var url = "http://127.0.0.1:3000/getBookImages";
          this.axios.get(url).then(result=>{
            this.mylist = result.data.result;
          })
         },


        getImages(){
          //完成一个功能,获取服务器端轮播图片
          //1:发送ajax请求
          var url = "http://127.0.0.1:3000/getImages";
          this.axios.get(url).then(result=>{
            this.list = result.data;
          })
          //2:获取返回数据保存list
        }
      },
    }  
    </script>
     <style>
     *{margin:0;padding:0;}
   .p2{
     margin-top:10px;
     width:100%;
     height:280px;  
   }
    .book_1{
    width:100%;
    height:100px;
    
    }
    .book_1 a{
      display:flex;
    }
.book_1 img{
   width:54px;
   height:66px;
   margin-left:5px;
   margin-top:5px;
 }
  .book_right{
   margin-left:10px;

  }
   .book_1 p{
  margin-bottom:5px;

   }
    /*轮播图设置父元素高度*/
    .app-home .mint-swipe{
      height:160px;
    }

    .app-home .mint-swipe img{
      width:100%;
      height:100%;
    }
    .mint-swipe .mint-swipe-indicators{
          bottom:0px;

    }
    .mt-swipe{
      z-index:1;
    }
    /*九宫格 图片大小 dpr 2*/
    .app-home .mui-grid-9 img{
      width:30px;
      height:30px;
    }
    /*九宫格  背景白色*/
    .app-home .mui-grid-view.mui-grid-9{
      background-color:#fff;
    }
    .app-home .mui-grid-view.mui-grid-9 li{
      border:0;
    }
    .mui-table-view .mui-col-xs-4{
      width:20%;
    }
    .deliever{
      width:100%;
      height:10px;
      background:#efefef;
                }
     .part1{
       width:100%;
    height:475px;
       }
       .zbtj{
       width:100%;
      height:40px;
       }
    .zbtj a{
     float:right;
      font-size:14px;
            }
               .zbtj h4{
                 float:left;
               }
                .top1{
                  width:100%;
                  height:200px;
                }
                  .top1 .p1{
                    clear:both;
                    display:flex;
                    justify-content:space-around;
                    width:100%;
                    list-style:none;
                  }
                    .top1 .p1 li{
                      padding-left:20px;
                 width:33.3333%; 
                  display:flex;
                  flex-direction:column;
                   justify-content:center;
                  
                    }
                     .top1 .p1 li img{
                        
                     width:80%;
                     height:80%; 

                     }
                          .top1 .p1 li div{

                     width:80%;
                     height:20%;
                     text-align:center;
                         overflow:hidden;
                         text-overflow:ellipsis;
                     }
                     .mint-search{
  position:fixed;
  z-index:10;
  top:0;
  width:100%;
}
.mint-searchbar{
   opacity:0.5;

}
.mint-searchbar-core{
   margin-top:15px;
}
input[type='search']{
  height:26px !important;
}

    </style>