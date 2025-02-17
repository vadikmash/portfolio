<script lang="ts">
	import { i18n } from '$lib/i18n';
	import { ParaglideJS } from '@inlang/paraglide-sveltekit';
	import Header from './components/Header/Header.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<ParaglideJS {i18n}>
	<div class="mx-auto max-w-[800px] px-3">
		<div class="flex min-h-screen flex-col">
			<Header />
			<main class="flex-1">
				{@render children()}
			</main>
		</div>

		<footer class="py-3">
			<div>© {new Date().getFullYear()} Vadzim Mashnitski</div>
			<a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA</a>
		</footer>
	</div>
</ParaglideJS>
