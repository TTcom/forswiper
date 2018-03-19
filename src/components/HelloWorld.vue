<template>
   <div class="swiperss">
          <slider swipeid='swipe01' :autoplay=3000>
          
	    <div class="swiper-slide" slot="swiper-con"><img src="../assets/images/banner/01.jpg"> </div>
	    <div class="swiper-slide" slot="swiper-con"><img src="../assets/images/banner/02.jpg"> </div>
	    <div class="swiper-slide" slot="swiper-con"><img src="../assets/images/banner/03.jpg"> </div>
          
          
          </slider>
         
         
   </div>
 
</template>

<script>
	
	import Slider from "../base/slider"
export default {
	components:{
		  Slider,
	},
	
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
