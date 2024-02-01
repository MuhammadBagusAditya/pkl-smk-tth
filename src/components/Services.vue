<script setup lang="ts">
import Card from "./ServiceCard.vue";

const services = [
	{
		title: "Tata Tertib",
	},
	{
		title: "Absensi Siswa",
	},
	{
		title: "Daftar PKL",
	},
];
</script>

<template>
	<div class="container mb-4">
		<h2 class="text-slate-900 text-3xl mb-1 font-bold text-center">Layanan</h2>

		<span class="block text-center text-slate-600 mb-6">Dapat berubah</span>

		<!-- cards -->
		<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3">
			<Card v-for="service in services" :key="service.title" :data="service" />
		</div>
		<!-- end cards -->
	</div>
</template>
