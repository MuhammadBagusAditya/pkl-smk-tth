<script setup lang="ts">
type cardProps = {
	title: string;
};

const props = defineProps<{
	data: cardProps;
}>();
</script>

<template>
	<div
		class="p-4 rounded-md border border-slate-900/20 shadow shadow-slate-900/20 flex flex-col items-center cursor-pointer"
		tabindex="0"
	>
		<img
			src="/img/gallery/a.jpg"
			alt="vite"
			class="w-[60%] aspect-[12/9] mb-3"
		/>

		<h3 class="text-2xl text-slate-800 font-semibold mb-3">
			{{ props.data.title }}
		</h3>
	</div>
</template>
