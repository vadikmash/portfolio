<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import Header from './components/Header/Header.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="mx-auto max-w-screen-md px-3">
		<div class="flex min-h-screen flex-col">
			<Header></Header>
			<main class="flex-1">
				{@render children()}
			</main>
		</div>

		<footer>
			<div>© 2024—2025</div>
			<a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA</a>
		</footer>
	</div>
</ParaglideJS>
