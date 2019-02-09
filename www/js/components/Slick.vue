<template>
<div class="slider-vue">
	<slick ref="slick" :options="slickOptions">
		<a href="#"><img src="http://placehold.it/2000x1000" alt=""></a>
		<a href="#"><img src="http://placehold.it/2000x1000" alt=""></a>
		<a href="#"><img src="http://placehold.it/2000x1000" alt=""></a>
		<a href="#"><img src="http://placehold.it/2000x1000" alt=""></a>
	</slick>
</div>
</template>

<script>
import Slick from 'vue-slick';
export default {
	components: {
		Slick
	},
	props: ['auto', 'fading'],
	data() {
		return {
			slickOptions: {
				slidesToShow: 1,
				dots: true,
				infinite: true,
				autoplay: this.auto,
				autoplaySpeed: 1800,
				fade: this.fading,
				responsive: [
					{
						breakpoint: 768,
						settings: {
							arrows: false
						}
					}
				]
			},
		};
	},
	methods: {

	},
	created() {

	}
};
</script>
