<template>
	<div class="tab-bar-item" @click="tabClick">
		<div v-if="!isActive"><slot name="tab-icon"></slot></div>
		<div v-else><slot name="tab-icon-active"></slot></div>
    <div :style="activeStyle"><slot name="tab-text"></slot></div>
		<!-- <div :class="{active:isActive}"><slot name="tab-text"></slot></div> -->
	</div>
</template>

<script>
	export default{
		name:'TabBarItem',
    props:{
      link:String,
      activeColor:{
        type:String,
        default:'red'
      }
    },
		data(){
			return{
				// isActive:true
			}
		},
    computed:{
      isActive(){
        //计数属性动态的决定isActive
        //拿到处于活跃的路径 里面是否有 this.path
        // /home => item(/home) =true
        return this.$route.path.indexOf(this.link) !== -1
      },
      activeStyle(){
         return this.isActive ? {color:this.activeColor} : {}
      }
    },
		methods:{
			tabClick(){
        // console.log(this.link)
        this.$router.push(this.link)
			}
		}
	}
</script>

<style scoped>

	.tab-bar-item{
		flex:1;
		text-align: center;
		height: 49px;
		margin-top:2px;
		font-size: 14px;
	}
	.tab-bar-item img{
		width: 24px;
		height: 24px;
		margin-bottom: 2px;
	}
	/* .active{
		color:#0c1b99;
	} */
</style>
