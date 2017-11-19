
<template>
	<transition name="fade" enter-active-class="animated slideInRight" leave-active-class="animated fadeOut"  >
			<main id="box">
				<div class="top">
					<router-link to="login">
						<p class="login">登录</p>
					</router-link>
					<router-link to="register">
						<p class="register">注册</p>
					</router-link>
					<!--<transition name="fade" enter-active-class="animated slideInLeft" leave-active-class="animated fadeOut"  >
						<component :is="msg"></component>
					</transition>-->
				</div>
		
		<ol>
			<li>账号：<input type="text" placeholder="请输入账号或手机号或邮箱" class="user"/><br/></li>
			<li>密码：<input type="password" placeholder="请输入密码" class="password"/><br/></li>
			<li>验证码：<input type="text" placeholder="请输入密码" class="yanzheng"/><br/></li>
		</ol>
	
	<div class="wrap">
		
		<input type="checkbox" class="check"/>
		<p class="other">同意注册条款</p>
		<button>注册</button>
	</div>
		
		
			
	</main>
	</transition>
</template>



<script>
//	export default{
//		data(){
//			return{
//				msg:'',
//			}
//		},
//		components:{
//			'aaa':{
//				template:'#con',
//				data(){
//					return {
//					msg:'login',
//					}
//					
//			},
//			components:{
//				'login':{
//					template:'#context',
//					data(){
//						return {
//							msg:'login'
//						}
//					}
//				},
//			'register':{
//				template:'<h1>注册界面</h1>'
//				},
//							
//			}
//			}
//		}
//	}
</script>

<style scoped>
	#box{
		width:100%;
		height: 100%;
		position: fixed;
		top:0;
		left:0;
		z-index: 10000;
		background: #fff;
	}
	.top{
		width:100%;
		height:8%;
		background: #f84056;
		overflow: hidden;
	}
	
	.top p{
		font-size:18px;
		color:#fff;
		margin-top:4%;
	}
	
	.login{
		margin-left:15%;
		float:left;
	}
	.register{
		float: right;
		margin-right:15%;
	}
	
	.nav{
		width:100%;
		/*height: 8%;*/
		height: 50px;
		border-bottom: 1px solid #ddd;
	}
	
	.nav>ul{
		overflow: hidden;
		width:100%;
		height:100%;
	}
	.nav>ul li{
		width:50%;
		height: 95%;
		float:left;
		font-size:14px;
		color:#333333;
		text-align: center;
		line-height: 50px;
	}
	
	.active{
		color:red !important;
		border-bottom: 2px solid red;
	}
	
	ol>li{
		width:100%;
		height: 40px;
		border:1px solid #ddd;
		margin-top: -1px;
		line-height: 40px;
		padding-left: 10px;
	}
	
	ol li input{
		width:80%;
		border:none;
		outline: none;
		padding-left: 10px;
	}
	
	button{
		width:95%;
		height:40px;
		margin: 20px 10px;
		background: #f84056;
		color:#fff;
		border:none;
		outline: none;
		text-align: center;
		line-height: 5%;
		font-size: 14px;
		border-radius:5px;
	}
	
	hr{
		width:95%;
		height: 1px;
		
	}
	
	.check{
		/*position: absolute;
		left:15%;
		top:10%;*/
		float:left;
		width:15px;
		height: 15px;
		margin-top:24px;
		margin-left:15px;
	}
	
	.other{
		width:30%;
		color:#999999;
		margin:20px auto;
		text-align: center;
		float:left;
	}
	
	.ways{
		width:100%;
	}
	
	.ways>ul{
		width:92%;
		overflow: hidden;
		margin: 30px 10%;
	}
	
	.ways>ul li{
		float:left;
		width:23%;
		margin-left:2%;
	}
	
	.ways>ul li img{
		width:35px;
		height: 30px;
	}
	
</style>