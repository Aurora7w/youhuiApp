<template>
	<main>
		<ul class="menu">
			<li class="thumb">
				<router-link to="home"><a href="javascript:;" class="tit">发现</a></router-link>
			</li>
			<li>
				<router-link to="skin"><a href="javascript:;" class="tit">极致美肤</a></router-link>
			</li>
			<li>
			   <router-link to="decoration"><a href="javascript:;" class="tit">个性配饰</a></router-link>
			</li>
			
			<li>
				<router-link to="hot"><a href="javascript:;" class="tit">本周热卖</a></router-link>
			</li>
		</ul>
		
		<!--轮播图-->
		<mt-swipe :auto="4000">
		  <mt-swipe-item><img src="../../assets/image/banner1.png" width="100%"  class="first"/></mt-swipe-item>
		  <mt-swipe-item><img src="../../assets/image/banner2.png" width="100%"  class="second"/></mt-swipe-item>
		</mt-swipe>
		<div class="icon-container">
		<ul class="icon">
			<li>
				<router-link to='hot'><img src="../../assets/image/logo1.png"/><span>保税区</span></router-link>
			</li>
			<li>
				<router-link to="order"><img src="../../assets/image/logo2.png"/><span>订单</span></router-link>	
			</li>
			<li>
				<router-link to="sort"><img src="../../assets/image/logo3.png"/><span>类目</span></router-link>	
			</li>
			<li>
				<router-link to="hot"><img src="../../assets/image/logo4.png"/><span>闪购</span></router-link>
			</li>
		</ul>
		</div>
		
		<!--<div class="context-tit">
			<ol>
				<li class="active">今日上新</li>-->
				<!--<li>明日预告</li>-->
			<!--</ol>
			
		</div>-->
		<!--<div class="context-show">
			<div class="container">
				<span class="slogo"><img src="../../assets/image/show.png" width="30px"/></span>
			<p>今日共有12个专场开售</p>
			<ul class="show">-->
				<!--<li></li>
				<li></li>
				<li></li>
				<li></li>-->
				<!--<li v-for="(v,i) in con" v-show="i==msg"></li>
			</ul>
			</div>
			
			
			
			
			
		</div>-->
		
	<div class="context-tit">
		<div class="nav">
     	 	<mt-button size="small" @click.native.prevent="active = 'tab-container1'" class="active2 tab1">今日上新</mt-button>
      		<mt-button size="small" @click.native.prevent="active = 'tab-container2'" class="tab2">明日预告</mt-button>
   		 </div>
	</div>
	
	
	<div class="wrap">
		
	
    <div class="container">
    	<div class="context-show">
    		<span class="slogo"><img src="../../assets/image/show.png" width="30px"/></span>
			<!--<p>今日共有12个专场开售</p>-->
			<marquee direction="left" class="scroll">今日共有12个专场开售</marquee>
    	</div>
			
	
    
    <div class="page-tab-container">
      <mt-tab-container class="page-tabbar-tab-container" v-model="active" swipeable>
        <mt-tab-container-item id="tab-container1">
        	
          <mt-cell v-for="n in list1" title=""><img v-lazy="n"/></mt-cell>
        </mt-tab-container-item>
        <mt-tab-container-item id="tab-container2">
        	<!-- cell组件 -->
          <mt-cell v-for="n in list2" title=""><img v-lazy="n"/></mt-cell>
        </mt-tab-container-item>
      </mt-tab-container>
    </div>
    
    </div>
    </div>
    
			
		
	</main>
</template>

<script type="text/javascript">
	export default{
//		name:'page-tab-container',
		data(){
			return{
				list1:['../src/assets/image/lunbo1.png','../src/assets/image/lunbo2.png','../src/assets/image/lunbo3.png','../src/assets/image/lunbo4.png'],
				list2:['../src/assets/image/lunbo5.png','../src/assets/image/lunbo6.png','../src/assets/image/lunbo7.png','../src/assets/image/lunbo8.png'],
				active:'tab-container1',
			}
		},
		methods:{
			
		},
		mounted(){
			
		}
	}
	
	
</script>

<style>
	.mint-swipe{
		width:100%;
		height:100%;
		/*padding-bottom:37%;*/
	}
	
	.mint-swipe-items-wrap{
		position: relative;
	    overflow: hidden;
	    height: 100%;
	    padding-bottom: 37%;
	}
	
	.mint-cell-wrapper{
		/*background-image: -webkit-linear-gradient(top, #fff, #fff 50%, transparent 50%);*/
		background-image: linear-gradient(180deg, #fff, #fff 50%, transparent 50%);
	}
	
	
	.mint-cell{
		width:100%;
		
	}
	
</style>

<style scoped>
	*{
		margin:0;
		padding:0;
		list-style:none;
		text-decoration: none;
	}
	
	main{
		background:#eee;
		margin-bottom:50px;
	}
	
	.menu{
		margin-bottom:5px;
		height: 50px;
	}
	
	.menu{
		width:100%;
		box-sizing:border-box;
		/*padding:10px 30px;*/
		overflow:hidden;
		background:#fff;
	}
	
	.thumb{
		border-bottom: 4px solid red;
	}
	
	.menu li{
		float:left;
		width:26%;
		height: 46px;
		text-align: center;
	}
	
	.menu li:nth-of-type(1){
		width:22%;
	}
	.menu>li .tit{
		font-size:18px;
		color:#333;
		line-height: 50px;
	}

	
	
	.icon-container{
		border:1px solid #ddd;
		margin-top:5px;
		padding:20px;
		background:#fff;
	}
	
	.icon{
		margin-left:20px;
		margin-top:20px;
		
		
		overflow: hidden;
	}
	.icon>li{
		float:left;
		width:20%;
		margin-right:10px;
	}
	.icon>li img{
		display:block;
		width:100%;
	}
	
	.icon>li span{
		display:block;
		font-size:14px;
		color:#333;
		margin:10px 0 0 5px;
	}
	
	.icon>li:nth-of-type(2) span{
		margin:10px 0 0 20px;
	}
	
	.icon>li:nth-of-type(3) span{
		margin:7px 0 0 20px;
	}
	
	.icon>li:nth-of-type(4) span{
		margin:10px 0 0 20px;
	}
	
	/*.context-tit{
		width:100%;
		height:0;
		padding-bottom: 20%;
		background: #fff;
		margin-top:-5px;
	}*/
	
	.context-tit{
		width:100%;
		overflow: hidden;
		height: 40px;
		background: #fff;
		margin-top:3px;
		padding:15px 0;
	}
	
	.context-tit .tab1{
		font-size:14px;
		color:#333;
		float:left;
		width:20%;
		background: #fff;
		border:none;
		outline: none;
		text-align: center;
		line-height:35px;
		margin: 0 15% 0 25%;	
	}
	
	.context-tit .tab2{
		font-size:14px;
		color:#333;
		float:left;
		width:20%;
		background: #fff;
		border:none;
		outline: none;
		text-align: center;
		line-height:35px;
	}
	
	
	.wrap{
		width:100%;
		height: auto;
		margin-top:1%;
		background: #fff;
		padding-bottom:20px;
	}
	
	.container{
		width:90%;
		margin:1% auto;
		
	}
	
	
	.context-show{
		overflow: hidden;
	
	}
	
	.slogo{
		display:block;
		float:left;
		margin-top:30px;
		margin-right:20px;
	}

	

	.container .page-tab-container img{
		width:100%;
		margin-top:1%;
		height: 100px;
	}
	
	.container>.context-show>.scroll{
		width:85%;
		font-size:14px;
		color:#999;
		float:left;
		margin-top:32px;
		margin-left:-10px;
	}
	
	.active2{
		color:#FF0000 !important;
	}
	
	
	
	
</style>