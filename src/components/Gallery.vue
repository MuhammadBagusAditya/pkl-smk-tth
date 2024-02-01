<script setup lang="ts">
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

const slides = [
	"/img/gallery/a.jpg",
	"/img/gallery/b.jpg",
	"/img/gallery/a.jpg",
	"/img/gallery/b.jpg",
];

const breakpoints = {
	600: {
		itemsToShow: 2.5,
	},
};
</script>

<template>
	<div class="container mb-4">
		<h2 class="text-slate-900 text-3xl mb-6 font-bold text-center">
			Galeri Foto
		</h2>

		<carousel :items-to-show="1" snap-align="start" :breakpoints="breakpoints">
			<slide v-for="slide in slides" :key="slide">
				<div class="relative aspect-video rounded-md overflow-hidden">
					<img :src="slide" alt="" class="w-full aspect-video" />

					<span
						class="absolute bottom-0 left-0 w-full bg-slate-900/70 text-slate-200 block text-center py-3 px-4 backdrop-blur-sm"
						>Pertemuan dengan Pembimbing Gamelab</span
					>
				</div>
			</slide>

			<template #addons>
				<navigation />
				<pagination />
			</template>
		</carousel>
	</div>
</template>

<style lang="postcss">
.carousel__track {
	@apply gap-0 sm:gap-3;
}
</style>
