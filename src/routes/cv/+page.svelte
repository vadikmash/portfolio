<script lang="ts">
	import type { PageData } from './$types';
	import avatarSource from '$lib/images/avatar.jpg';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Vadzim Mashnitski - CV</title>
	<meta name="description" content="Vadzim Mashnitski's CV" />
</svelte:head>

<section class="flex flex-wrap items-start justify-between gap-y-5">
	<div class="flex items-center gap-5">
		<img
			src={avatarSource}
			alt="Vadzim Mashnitski"
			class="-ml-0 h-[100px] w-[100px] rounded-full"
		/>
		<div class="flex flex-col justify-center">
			<h2 class="mb-2 text-2xl font-bold">Vadzim Mashnitski</h2>
			<h3 class="font-thin text-gray-400">Full-Stack Software Engineer</h3>
		</div>
	</div>
	<div class="pr-20 md:pt-5">
		<h4 class="text-xl font-bold">Contact info</h4>

		<div class="mt-3 md:basis-1/3">
			<ul class="flex flex-wrap gap-x-3 gap-y-1 md:flex-col">
				<li><a href="mailto:vadikmash@gmail.com">vadikmash@gmail.com</a></li>
				<li><a href="https://github.com/vadikmash">GitHub</a></li>
				<li><a href="https://linkedin.com/in/vadikmash">LinkedIn</a></li>
				<li><a href="https://x.com/vadikmash">X (Twitter)</a></li>
			</ul>
		</div>
	</div>
</section>
