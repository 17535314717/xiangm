<template>
  <div id="content">
    <div id="header">
      <h2><img :src="user.icon" alt=""/></h2>
      <div class="user-box">
        <a >{{user.nikename}}</a>&nbsp;&nbsp;&nbsp;&nbsp;
        <a @click="logout">注销</a>
      </div>
      <ul class="clear">
        <li>
          <!-- <span>{{$route.query.user.follow}}</span> -->
          <span>{{user.follow}}</span>
          <p>关注</p>
        </li>
        <li>
          <!-- <span>{{$route.query.user.fans}}</span> -->
          <span>{{user.fans}}</span>
          <p class="end">粉丝</p>
        </li>
      </ul>
    </div>
    <div class="docList">
      <ul>
        <li class="gk-text">
          <i></i>
          <p>公开博文</p>
          <b></b>
          <span>0</span>
        </li>
        <li class="mm-text">
          <i></i>
          <p>秘密博文</p>
          <b></b>
          <span>0</span>
        </li>
        <li class="cg-text">
          <i></i>
          <p>草稿箱</p>
          <b></b>
          <span>0</span>
        </li>
        <li class="sc-text">
          <i></i>
          <p>收藏夹</p>
          <b></b>
          <span>0</span>
        </li>
        <li class="my_cz">
          <i></i>
          <p>收藏夹</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  //import 组件名称 from '组件路径’
import axios from '../plugins/axios.js'
  export default {
    name:'user',
    props:{},
	
    data(){
      return {
        user:this.$route.query.user
      }
    },
	beforeRouteEnter(to,from,next) {
		// 自动登录
		axios({
			url:'/api/user',
			
		}).then(
		// 如果err=0,就上边user对象里的信息 =res.data.data
			res=> {
				if(res.data.err===0){
					to.query.user=res.data.data
					next() 
				}else{
					next('/login')
				}
			}
		)
	},
    components:{},
    //生命周期 - 挂载完成
    mounted(){
		
	},
   //生命周期 - 更新完成
    updated(){},
   //方法集合
    methods:{
		logout(){
			window.localStorage.removeItem('user');
			this.$router.push('/login')
		}
	},
   //生命周期 - 销毁完成
    destroyed(){

    }
  }
</script>

<style scoped>
  
  #content{max-width:6.4rem; margin:0 auto; margin-bottom:0.8rem;}
  #content #header{width:6.4rem;height:2.84rem; background:#e54847; padding-top:0.4rem;}
  #header h2{width:1.02rem;height:1.02rem; border-radius:50%; margin:0 auto;}
  #header h2 img{width:100%;}
  #header .user-box{width:1.5rem; font-size:0.25rem; color:#fff; margin:0 auto; margin-top:0.2rem;}
  .user-box a{color:#fff;}
  #header ul{ margin-top:0.4rem;}
  #header ul li{width:50%;height:0.7rem; float:left; color:#fff;}
  #header ul li span{height:0.37rem; line-height:0.37rem; text-align:center; display:block; font-size:0.25rem;}
  #header ul li p{ text-align:center; font-size:0.3rem;height:0.32rem; line-height:0.32rem; border-right:1px solid #fff;}
  #header ul li p.end{ border:0;}
  
  #content .docList{width:6.4rem; margin:0 auto; margin-top:0.32rem;}
  .docList ul{ border-top:1px solid #7b7c7c;}
  .docList ul li{ background:#fff;height:0.79rem; border-top:1px solid #bcbbba; border-bottom:1px solid #7b7c7c;}
  .docList ul li span{ float:right;margin-right:0.14rem; margin-top:0.26rem;}
  .docList ul li b{width:0.21rem;height:0.24rem; background:url(../assets/img/next_img.png) no-repeat 0 0; background-size:100%; float:right;margin-right:0.34rem; margin-top:0.28rem;}
  
  
  .docList ul .gk-text i{width:0.37rem;height:0.37rem; background:url(../assets/img/gk_text.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.29rem; margin-top:0.24rem;}
  .gk-text p{ float:left; font-size:0.25rem;margin-left:0.29rem; margin-top:0.25rem;}
  .docList ul .mm-text i{width:0.29rem;height:0.35rem; background:url(../assets/img/mm_text.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.32rem; margin-top:0.24rem;}
  .mm-text p{ float:left; font-size:0.25rem;margin-left:0.35rem; margin-top:0.25rem;}
  .docList ul .cg-text i{width:0.37rem;height:0.37rem; background:url(../assets/img/cg_text.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.29rem; margin-top:0.24rem;}
  .cg-text p{ float:left; font-size:0.25rem;margin-left:0.29rem; margin-top:0.25rem;}
  .docList ul .sc-text i{width:0.37rem;height:0.37rem; background:url(../assets/img/sc_text.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.29rem; margin-top:0.24rem;}
  .sc-text p{ float:left; font-size:0.25rem;margin-left:0.29rem; margin-top:0.25rem;}
  .docList ul .my_cz{ margin-top:0.45rem;}
  .docList ul .my_cz i{width:0.37rem;height:0.37rem; background:url(../assets/img/my_cz.png) no-repeat 0 0; background-size:100%; float:left; margin-left:0.29rem; margin-top:0.24rem;}
  .my_cz p{ float:left; font-size:0.25rem;margin-left:0.29rem; margin-top:0.25rem;}
</style>
