<script lang="ts">
	import { page } from '$app/state';

	const { label, path, isHeader = false, imageSource = '', imageAlt = '' } = $props();
</script>

<li aria-current={page.url.pathname === path ? 'page' : undefined}>
	{#if page.url.pathname === path && isHeader}
		<h1 class="flex items-center justify-center">
			{#if imageSource}
				<a href={path} class="border-none">
					<img src={imageSource} alt={imageAlt} class="mr-2 h-9 w-9 rounded-full" />
				</a>
			{/if}
			<a href={path} class="border-none font-bold text-current">
				{label}
			</a>
		</h1>
	{:else}
		<span class="flex items-center justify-center">
			{#if imageSource}
				<a href={path} class="border-none">
					<img src={imageSource} alt={imageAlt} class="mr-2 h-9 w-9 rounded-full" />
				</a>
			{/if}
			<a href={path} class={page.url.pathname === path ? 'border-none font-bold text-current' : ''}>
				{label}
			</a>
		</span>
	{/if}
</li>
