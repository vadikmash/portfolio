<script lang="ts">
	import { base } from '$app/paths';
	import { page } from '$app/state';
	import NavLink from './components/NavLink.svelte';
	import avatarSource from '$lib/images/avatar.jpg';

	const isCvPage = $derived(page.url.pathname.includes('/cv'));
</script>

<header class="flex w-full justify-center py-6">
	<nav class="flex w-full justify-between">
		<ul class="flex items-center gap-4 md:gap-6">
			<NavLink
				label="Vadzim Mashnitski"
				path={`${base}/`}
				isHeader
				alternativeLabel={isCvPage ? 'Home' : ''}
				imageSource={avatarSource}
				imageAlt="avatar"
				hideImage={isCvPage}
			/>
			<NavLink label="Projects" path={`${base}/projects`} />
			<NavLink label="Blog" path={`${base}/blog`} />
		</ul>
	</nav>
</header>
