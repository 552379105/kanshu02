    <template>  
       <!--第一部分:顶部导航栏-->
        <div class="shoplist">  
            <mt-header fixed title="书架">   </mt-header>
       <!--通知-->
            <div class="ad"> 新用户首次登陆,送7天VIP
                <span class="mui-icon mui-icon-forward" style=" line-height:30px;float:right;"> </span>
            </div>
    <!-- 第二部分书架展示 -->
         <ul class="showbook" >
            <li class="book_2"
               v-for="tmp of list" :key="tmp.id">
                <img :src="tmp.book_url"/>
                <div class="book_2l">
                  <div>{{tmp.name}} </div>
                </div>
            </li>
         </ul>
    <!---->

        </div>
    </template>
    <script>
         import {Toast} from "mint-ui";
       export default {
      data(){
       return {
         list:[],//返回数据
       } 
       },
     created() {
          //当组件对象创建成功后即可发送ajax请求
          this.getImages();
      },
       methods:{
           getImages(){
               var url ="http://127.0.0.1:3000/getBookImages2";
               this.axios.get(url).then(result=>{
                   this.list = result.data.result;
               })
           }
       },
    }
    </script>

    <style>
         *{margin:0px;padding:0px;}
  .mint-header{
             background:#fff !important;
             color:#000 !important;
             
         }
      .ad{  
          margin-top:50px;
    width:100%;
    height:30px;
    background:#ccc;
     border-radius:20px;
     color:#000;
     font-size:13px;
     text-align:center;
     line-height:30px;
      }   
   .showbook{      
     display:flex;
     flex-wrap:wrap;
     width:100%;
     list-style:none;
      margin-top:20px;
   }
   .book_2{
       font-size:12px;
     width:33.3333%;
     height:150px;
     text-align:center;
     }
     .book_2 img{
       width:80%;
       height:80%;
     }


    </style>

