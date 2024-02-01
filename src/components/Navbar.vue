<script setup lang="ts">
import { ref, Ref } from "vue";
import { BIconList } from "bootstrap-icons-vue";

const isTransparent: Ref<Boolean> = ref(false);

const isLinksShowed: Ref<Boolean> = ref(false);

document.addEventListener("scroll", function () {
	isTransparent.value = window.scrollY > 100;
});
</script>

<template>
	<nav
		class="w-full py-4 fixed top-0 left-0 transition z-10"
		:class="{ 'bg-slate-900': isTransparent }"
	>
		<div class="container flex justify-between items-center gap-6">
			<h1 class="text-xl sm:text-3xl text-slate-100">PKL SMK TTH</h1>

			<div
				class="flex flex-col sm:flex-row gap-6 sm:gap-4 fixed sm:static left-0 bg-slate-900/80 sm:bg-inherit backdrop-blur-sm sm:backdrop-blur-0 w-full sm:w-auto h-screen sm:h-auto items-center pt-20 sm:pt-0 transition-all"
				:class="{ 'top-0': isLinksShowed, 'top-[-100%]': !isLinksShowed }"
				@click="isLinksShowed = false"
			>
				<a
					href="#"
					class="text-slate-200 text-2xl sm:text-lg drop-shadow shadow-slate-900/20"
					>Home</a
				>
				<a
					href="#"
					class="text-slate-200 text-2xl sm:text-lg drop-shadow shadow-slate-900/20"
					>Jurnal</a
				>
				<a
					href="#"
					class="text-slate-200 text-2xl sm:text-lg drop-shadow shadow-slate-900/20"
					>Layanan</a
				>
				<a
					href="#"
					class="text-slate-200 text-2xl sm:text-lg drop-shadow shadow-slate-900/20"
					>Galeri</a
				>
				<a
					href="#"
					class="text-slate-200 text-2xl sm:text-lg drop-shadow shadow-slate-900/20"
					>Mitra</a
				>
			</div>

			<button class="block sm:hidden" @click="isLinksShowed = true">
				<BIconList class="text-slate-200 text-3xl" />
			</button>
		</div>
	</nav>
</template>
