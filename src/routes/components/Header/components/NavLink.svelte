<script lang="ts">
	import { page } from '$app/state';
	import { base } from '$app/paths';

	const {
		label,
		path,
		isHeader = false,
		alternativeLabel = '',
		imageSource = '',
		imageAlt = '',
		hideImage = false
	} = $props();

	const isCurrentPath = $derived(
		page.url.pathname.slice(1).startsWith(path || '/') || page.url.pathname === path
	);
</script>

<li aria-current={isCurrentPath ? 'page' : undefined}>
	{#if isCurrentPath && isHeader}
		<h1 class="flex items-center justify-center">
			{#if imageSource}
				<a href={path} class={`border-none ${hideImage ? 'w-0' : ''}`}>
					<img
						src={imageSource}
						alt={imageAlt}
						class={`mr-2 h-9 w-9 rounded-full ${hideImage ? 'w-0' : ''}`}
					/>
				</a>
			{/if}
			<a href={path} class="border-none font-bold text-current">
				{alternativeLabel || label}
			</a>
		</h1>
	{:else}
		<span class="flex items-center justify-center">
			{#if imageSource}
				<a href={path} class={`border-none ${hideImage ? 'w-0' : ''}`}>
					<img
						src={imageSource}
						alt={imageAlt}
						class={`mr-2 h-9 w-9 rounded-full ${hideImage ? 'w-0' : ''}`}
					/>
				</a>
			{/if}
			<a href={path} class={isCurrentPath ? 'border-none font-bold text-current' : ''}>
				{alternativeLabel || label}
			</a>
		</span>
	{/if}
</li>
