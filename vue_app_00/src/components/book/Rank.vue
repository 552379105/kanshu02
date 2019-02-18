<template>
  <div class="Rank_containter"> 
   	<header class="mui-bar mui-bar-nav" style="background:blue;">
			<a class="mui-action-back mui-icon mui-icon-left-nav mui-pull-left"></a>
			<h1 class="mui-title"> 排行榜 </h1>
            <!-- 右上角弹出按钮-->
            <button class="Rank_button" v-on:click="Rank_list()">周榜 
            <span class="mui-icon mui-icon-arrowdown Rank_arrowd"></span>
            </button>
	</header>
      <!-- 右上角弹出菜单-->
      <div class="Rank_list" v-bind:class="Rank_classOject"> 
           <div> </div>  
           <div class="Rank_listbody"> 
            <ul  class="Rank_listbody">
                <li v-for="(item,i) in list"  v-on:click="Rank_listarw()" class="Rank_item">
                <a href="#" style="color:#000;">{{item}} </a>
                </li>   
            </ul> 
           
           </div> 
           
      </div>
         <div class="sexbookshelf">
             <div class="commonz" v-bind:class="Rank_classOjectB" v-on:click="SexIsOnm()">
             男频
             </div>
            <div class="commonz" v-bind:class="Rank_classOjectC" v-on:click="SexIsOnw()">
             女频
             </div>

 
         </div>
           <div class="deliever"></div>
         <div class="book_content">
            <div class="sexbookshelfleft">
              <a href="#" class="bookshelf_item" v-on:click="Rank_changeA()">畅销榜 </a>
              <a href="#" class="bookshelf_item" v-on:click="Rank_changeB()" >新书榜 </a>
              <a href="#" class="bookshelf_item" v-on:click="Rank_changeC()" >热搜榜 </a>
            </div>
            <div id="segmentedControlContents" >
                 <div id="content1" class="sgts_item" v-bind:class="Rank_classOjectD"> 
                    <ul>
                        <li>
                           content1
                        </li>
                    </ul>
                 </div>
            
                 <div id="content2" class="sgts_item" v-bind:class="Rank_classOjectE"> 
                    <ul>
                        <li>
                           content2
                        </li>
                    </ul>
                 </div>

                   <div id="content3" class="sgts_item" v-bind:class="Rank_classOjectF"> 
                    <ul>
                        <li>
                            content3
                        </li>
                    </ul>
                 </div>

            </div>
             
         
         </div>

       
     </div>
</template>
<script>
     export default{ 
      created(){},
       data(){  
           return{
                classA:true,
                classB:true,
                Rank_classOjectC:"",
                Rank_classOject:"",
                Rank_classOjectB:"activez",
                Rank_classOjectD:"",
                Rank_classOjectE:"",
                Rank_classOjectB:"",

               list:[
                   '周榜',
                    '月榜',
                    '总榜'
               ]
           }
         },
         methods:{
             Rank_list(){
               if(this.classA==true){     
                    this.Rank_classOject="Rank_list_show";
                    this.classA=false;
               }
               else if(this.classA==false){
                   this.Rank_classOject="";
                   this.classA=true
               }
             },
             SexIsOnm(){
                       this.Rank_classOjectB="activez";
                      this.Rank_classOjectC="";
                      
             },
               SexIsOnw(){
                       this.Rank_classOjectB="";
                      this.Rank_classOjectC="activez";
                      
             },
             Rank_changeA(){
                 Rank_classOjectD="Rank_active";
                 Rank_classOjectE="";
                 Rank_classOjectB="";
             },
             Rank_changeB(){
                 Rank_classOjectD="";
                 Rank_classOjectE="Rank_active";
                 Rank_classOjectB="";
             },
             Rank_changeC(){
                 Rank_classOjectD="";
                 Rank_classOjectE="";
                 Rank_classOjectB="Rank_active";
             }
               
         }
     }

</script>
<style >
*{
    margin:0;
    padding:0;
    list-style:none;
}
.book_content{
    width:100%;
    height:1000px;
    display:flex;
}
 .Rank_active{
  display:block !important;
 }
.sgts_item{

    display:none;
    width:100%;
    height:50px;
    border-bottom:2px solid #f00;
}
 #segmentedControlContents{
       width:85%;
       height:1000px;
       background:#fff;
}
.bookshelf_item{

    width:100%;
    height:50px;
    text-align:center;
    line-height:50px;
    color:#000;

}
.sexbookshelfleft{
    margin-top:2px;
    width:15%;
    background:#ccc;
    height:1000px;

}
.Rank_list_show{
    display:block !important;
}
.Rank_item{
 
    width:100%;
    height:33.33%;
    text-align:center;
    line-height:40px;
}
.Rank_listbody{
    width:100%;
    height:100%;
    
}
  .Rank_list{
       background:#fff;
      position:fixed;
      top:50px;right:17px;
      width:80px;
      height:120px;
      border:1px solid #ccc;
  display:none;
  }
 .Rank_arrowd{
    margin:0 !important;
    padding:0 !important;
    width:12px  !important;
    height:8px !important;
    right:7px;
}
.Rank_button{
      margin:0;
    padding:0;
    width:55px;
    height:34px;
    position:absolute;
    right:10px; top:5px;
    border-radius:20px;
}
.deliever{
    width:100%;
    height:2px;
     background:#ccc;
}
  .sexbookshelf{
      display:flex;
      margin-top:50px;
      width:100%;
      height:40px;
  }  
  .commonz{
      text-align:center;
      width:50%;
      border:10px;
      border:#000;
      font-size:17px;
      line-height:40px;
  }
  .activez{
      color:#007aff;
      border-bottom:3px solid #007aff;
  }
</style>