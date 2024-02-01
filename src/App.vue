<script setup lang="ts">
import Navbar from "./components/Navbar.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Journal from "./components/Journal.vue";
import Services from "./components/Services.vue";
import Gallery from "./components/Gallery.vue";
import Partners from "./components/Partners.vue";
import Footer from "./components/Footer.vue";

import { ref, onMounted } from "vue";

import { BIconChevronUp } from "bootstrap-icons-vue";

const win = ref<Window>();

onMounted(() => {
	win.value = window;
});
</script>

<template>
	<Navbar />

	<Jumbotron />

	<Journal />

	<Services />

	<Gallery />

	<Partners />

	<Footer />

	<button
		class="p-3 rounded-full fixed bottom-4 right-4"
		@click="() => win?.scrollTo({ top: 0 })"
	>
		<BIconChevronUp class="text-4xl text-slate-800" />
	</button>
</template>

<style>
body {
	scroll-behavior: smooth;
}
</style>
