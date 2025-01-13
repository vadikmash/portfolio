<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import Header from './Header.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div>
		<div class="min-h-screen flex flex-col">
			<Header></Header>
			<main class="flex-1 px-6">
				{@render children()}
			</main>
		</div>

		<footer class="p-6">
			<div>© 2024—2025</div>
			<a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA</a>
		</footer>
	</div>
</ParaglideJS>
