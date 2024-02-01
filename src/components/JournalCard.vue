<script setup lang="ts">
type cardProps = {
	title: string;
	icon: any;
};

const props = defineProps<{
	data: cardProps;
}>();
</script>

<template>
	<div
		class="p-4 rounded-md border border-slate-900/20 shadow shadow-slate-900/20 flex flex-col items-center"
	>
		<!-- <img src alt="vite" class="w-[20%] mb-3" /> -->
		<component
			:is="props.data.icon"
			class="w-[20%] text-5xl text-slate-700 mb-3"
		/>

		<h3 class="text-xl text-slate-800 font-semibold mb-3">
			{{ props.data.title }}
		</h3>

		<button class="py-2 px-4 rounded-md bg-emerald-600 text-slate-200">
			Buka
		</button>
	</div>
</template>
