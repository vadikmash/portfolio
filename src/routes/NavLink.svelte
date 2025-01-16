<script lang="ts">
	import { page } from '$app/state';

	const { label, path, isHeader = false } = $props();
</script>

<li aria-current={page.url.pathname === path ? 'page' : undefined}>
	{#if page.url.pathname === path && isHeader}
		<h1>
			<a href={path} class="border-none font-bold text-current">{label}</a>
		</h1>
	{:else if page.url.pathname === path}
		<a href={path} class="border-none font-bold text-current">{label}</a>
	{:else}
		<a href={path}>{label}</a>
	{/if}
</li>
