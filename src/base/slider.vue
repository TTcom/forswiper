<template>
		<div class="swiper-container" :class="swipeid">
		<div class="swiper-wrapper">
			
			<slot name='swiper-con'></slot>


		</div>
		<!--<img src="../assets/images/homebaner9_02.jpg">-->
	<div :class='{"swiper-pagination":pagination}' :style='{"text-align": pagenation}'></div>
  

	</div>

	 
	
	
</template>

<script>
	import '../assets/swiper/swiper.js'
	export default{
		
		props:{
			//以备多个轮播图
			swipeid:{               
				type:String,
				default:""			
			},
			//是否需要分页器
			pagination:{
				type:Boolean,
				default:true			
			},
			
			//分页器位置
			pagenation:{
				type:String,
				default:"center"
			},
			//切换效果
			effect:{
				type:String,
				default:'slide'
			},
			//是否轮播
			loop:{
				type:Boolean,
				default:true
			},
			//轮播方向
			direction:{
				type:String,
				default:'horizontal'
			},
			//轮播速度
			autoplay:{
				type:Number,
				default:2000
			},
			//分页器样式
			paginationType:{
				type:String,
				default:'bullets'
			}
			
		},
		//挂zai完成后创建插件对象swiper
		mounted(){
			var that=this
			new Swiper('.'+that.swipeid,{
				autoplayDisableOnInteraction : false, 
				loop: that.loop,
				pagination:'.swiper-pagination',
				paginationType: that.paginationType,
				autoplay:that.autoplay,
				prevButton:'.swiper-button-prev',
				nextButton:'.swiper-button-next',
				
			});
		}
		
	}
	
	
	
	
</script>

<style>
	@import '../assets/swiper/swiper.css';

	.swiper-container img{width:100%;}
	.swiper-pagination-bullet-active{background: white;}
	.swiper-button-prev, .swiper-button-next{top:65%}
	
	
	
</style>