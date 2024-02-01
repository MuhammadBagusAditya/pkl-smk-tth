<script setup lang="ts">
import Card from "./JournalCard.vue";
import {
	BIconCodeSquare,
	BIconPcDisplay,
	BIconPalette2,
	BIconCarFrontFill,
} from "bootstrap-icons-vue";

const journals = [
	{
		title: "RPL",
		icon: BIconCodeSquare,
	},
	{
		title: "TKJ",
		icon: BIconPcDisplay,
	},
	{
		title: "MM",
		icon: BIconPalette2,
	},
	{
		title: "TKR",
		icon: BIconCarFrontFill,
	},
];
</script>

<template>
	<div class="container mb-4">
		<h2 class="text-slate-900 text-3xl mb-1 font-bold text-center">
			Jurnal Guru
		</h2>

		<span class="block text-center text-slate-600 mb-6">Mingguan</span>

		<!-- cards -->
		<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3">
			<Card v-for="journal in journals" :key="journal.title" :data="journal" />
		</div>
		<!-- end cards -->
	</div>
</template>
