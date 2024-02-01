<script setup lang="ts">
const partners = [
	"/img/partners/gamelab.png",
	"/img/partners/gamelab.png",
	"/img/partners/gamelab.png",
	"/img/partners/gamelab.png",
	"/img/partners/gamelab.png",
	"/img/partners/gamelab.png",
];
</script>

<template>
	<div class="container mb-4">
		<h2 class="text-slate-900 text-3xl mb-6 font-bold text-center">
			Mitra Kami
		</h2>

		<div
			class="grid grid-cols-2 sm:grid-cols-[repeat(auto-fill,_200px)] justify-around gap-3"
		>
			<div v-for="partner in partners" :key="partner">
				<img :src="partner" alt="" class="w-full" />
			</div>
		</div>
	</div>
</template>

<style>
.carousel__track {
	gap: 1rem;
}
</style>
