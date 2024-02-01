<script setup lang="ts"></script>

<template>
	<!-- jumbotron -->
	<div
		class="w-full min-h-[80vh] mb-4 bg-cover bg-center flex"
		style="background-image: url('/img/banner.svg')"
	>
		<div
			class="container grid grid-cols-1 grid-rows-2 md:grid-cols-[400px,_1fr] md:grid-rows-1"
		>
			<div class="grid place-items-center pt-20 md:pt-0">
				<img src="/img/logo.png" alt="logo" class="w-[35vw] max-w-[10rem]" />
			</div>

			<div class="md:pt-40">
				<span
					class="text-slate-200 text-xl md:text-2xl mb-3 block text-center md:text-left"
				>
					Selamat Datang di
				</span>

				<h1
					class="text-slate-100 text-3xl lg:text-4xl font-semibold mb-6 text-center md:text-left"
				>
					Website layanan PKL <br />
					SMK TTH
				</h1>

				<button
					class="py-2 px-4 rounded-md bg-emerald-600 text-slate-200 mx-auto md:mx-0 block"
				>
					See More
				</button>
			</div>
		</div>
	</div>
	<!-- end jumbotron -->
</template>
