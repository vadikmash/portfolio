<script lang="ts">
	import { page } from '$app/stores';
</script>

<header class="flex w-full justify-center p-6 pb-10">
	<nav class="flex justify-between w-full">
		<ul class="flex gap-4">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				{#if $page.url.pathname === '/' }
					<h1>
						<a href="/" class="font-bold text-black shadow-none">Vadzim Mashnitski</a>
					</h1>
				{:else}
					<a href="/">Vadzim Mashnitski</a>
				{/if}
			</li>
			<li aria-current={$page.url.pathname.includes('/projects') ? 'page' : undefined}>
				<a href="/projects">Projects</a>
			</li>
			<li aria-current={$page.url.pathname.includes('/cv') ? 'page' : undefined}>
				<a href="/cv">CV</a>
			</li>
			<li aria-current={$page.url.pathname.includes('/blog') ? 'page' : undefined}>
				<a href="/blog">Blog</a>
			</li>
		</ul>
	</nav>
	
</header>