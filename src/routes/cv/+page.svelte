<script lang="ts">
	import type { PageData } from './$types';
	import avatarSource from '$lib/images/avatar.jpg';

	let { data }: { data: PageData } = $props();

	const today = new Date();
	const beginningOfCareer = new Date(2019, 0, 15);
	const millisecondsInYear = 1000 * 60 * 60 * 24 * 365;
	const yearsOfExperience = Math.floor(
		(today.getTime() - beginningOfCareer.getTime()) / millisecondsInYear
	);
</script>

<svelte:head>
	<title>Vadzim Mashnitski - CV</title>
	<meta name="description" content="Vadzim Mashnitski's CV" />
</svelte:head>

<section
	class="mt-3 flex flex-col items-start justify-between gap-5 border-b border-gray-200 pb-6 md:flex-row"
>
	<div class="md:basis-2/3">
		<div class="flex items-center gap-5">
			<img
				src={avatarSource}
				alt="Vadzim Mashnitski"
				class="-ml-0 h-[70px] w-[70px] rounded-full"
			/>
			<div class="flex flex-col">
				<h2 class="text-2xl font-bold md:text-3xl">Vadzim Mashnitski</h2>
				<h3 class="mt-1 text-xs font-thin text-gray-400 md:text-sm">
					Full-Stack Software Engineer | Web Architect
				</h3>
			</div>
		</div>
	</div>

	<ul class="flex flex-wrap gap-x-4 gap-y-1 md:flex-col md:items-end">
		<li><a href="mailto:vadikmash@gmail.com">vadikmash@gmail.com</a></li>
		<li><a href="https://github.com/vadikmash">GitHub</a></li>
		<li><a href="https://linkedin.com/in/vadikmash">LinkedIn</a></li>
	</ul>
</section>

<section class="mt-5 border-b border-gray-200 pb-6">
	<ul class="flex flex-col gap-3">
		<li>
			<strong>Summary:</strong> Professional Full Stack Software Engineer with more than {yearsOfExperience}
			years of web & mobile development experience.
		</li>
		<li><strong>Years of experience:</strong> {yearsOfExperience}+</li>
		<li><strong>English:</strong> Advanced (C1)</li>
	</ul>
</section>

<section class="mt-5 border-b border-gray-200 pb-6">
	<h4 class="text-xl font-bold">Technical Skills</h4>
</section>

<section class="mt-5 border-b border-gray-200 pb-6">
	<h4 class="text-xl font-bold">Professional experience</h4>
</section>

<section class="mt-5 flex flex-wrap items-start justify-between gap-y-5">
	<h4 class="text-xl font-bold">Education</h4>

	<ul class="flex flex-col gap-y-3">
		<li>
			<strong><a href="https://bsu.by"> Belarusian State University</a></strong>
			(2018 - 2022):<br />
			Bachelor degree in Applied Informatics (Faculty of Radiophysics and Computer Technologies)
		</li>
		<li>
			<strong
				><a href="https://school.rollingscopes.com/" target="_blank">
					The Rolling Scopes School</a
				></strong
			>
			(2019):<br />
			<a href="https://app.rs.school/certificate/n4la9xpk">Certificate</a>
		</li>
	</ul>
</section>
