<script lang="ts">
	import NavLink from './NavLink.svelte';
</script>

<header class="flex w-full justify-center p-6 pb-10">
	<nav class="flex w-full justify-between">
		<ul class="flex gap-4">
			<NavLink label="Vadzim Mashnitski" path="/" isHeader />
			<NavLink label="Projects" path="/projects" />
			<NavLink label="CV" path="/cv" />
			<NavLink label="Blog" path="/blog" />
		</ul>
	</nav>
</header>
