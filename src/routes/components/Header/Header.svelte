<script lang="ts">
	import NavLink from './components/NavLink.svelte';
	import avatarSource from '$lib/images/avatar.jpg';
</script>

<header class="flex w-full justify-center py-6">
	<nav class="flex w-full justify-between">
		<ul class="flex items-center gap-4 md:gap-6">
			<NavLink
				label="Vadzim Mashnitski"
				path="/"
				isHeader
				imageSource={avatarSource}
				imageAlt="avatar"
			/>
			<NavLink label="Projects" path="/projects" />
			<NavLink label="CV" path="/cv" />
			<NavLink label="Blog" path="/blog" />
		</ul>
	</nav>
</header>
