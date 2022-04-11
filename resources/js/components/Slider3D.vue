<template>
	<swiper
		:effect="'coverflow'"
		:grabCursor="true"
		:centeredSlides="true"
		:slidesPerView="'auto'"
		:coverflowEffect="{
			rotate: 70,
			stretch: 0,
			depth: 100,
			modifier: 1,
			slideShadows: true,
		}"
		:autoplay="{
			delay: 2000,
			disableOnInteraction: false,
		}"
		:loop="true"
		:modules="modules"
		:scrollbar="{draggable: true}"
		class="container mx-auto h-96"
	>
		<!-- <swiper-slide class="relative flex justify-center items-center bg-transparent" v-for="collection in 4" :key="collection">
			<img class="h-full w-full object-cover" src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="img" />
		</swiper-slide> -->
		<swiper-slide class="relative flex justify-center items-center bg-transparent" v-for="collection in collections" :key="collection">
			<img class="h-full w-full object-cover" :src="collection.imgUrl" alt="img" />
		</swiper-slide>
	</swiper>
</template>
<script>
// Import Swiper Vue.js components
import {Swiper, SwiperSlide} from "swiper/vue"

// Import Swiper styles
import "swiper/css"
import "swiper/css/effect-coverflow"
import "swiper/css/autoplay"
// import required modules
import {EffectCoverflow, Autoplay} from "swiper"

export default {
	props: {
		collections: Array,
	},
	components: {
		Swiper,
		SwiperSlide,
	},
	setup() {
		return {
			modules: [EffectCoverflow, Autoplay],
		}
	},
}
</script>

<style scoped>
.swiper {
	width: 100%;
	padding-top: 20px;
	padding-bottom: 20px;
}

.swiper-slide {
	background-position: center;
	background-size: cover;
	width: 400px !important;
	height: 300px !important;
}

.swiper-slide img {
	display: block;
	width: 100%;
}
</style>
