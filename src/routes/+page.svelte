<script lang="ts">
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Vadzim Mashnitski - Home</title>
	<meta name="description" content="Vadzim Mashnitski's Home Page" />
</svelte:head>

<section>
	<h1>
		<!-- <span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcomeFallback} alt="Welcome" />
			</picture>
		</span> -->

		Vadzim Mashnitski 
	</h1>

	<p>
		I'm a software engineer, creator, musician. I specialize in web/mobile apps architecture and full-stack development.
		When not busy with my main job, I create my own cool apps and services, write songs, travel.  
	</p>

	<div>
		<ul>
			<li><a href="mailto:vadikmash@gmail.com">vadikmash@gmail.com</a></li>
			<li><a href="https://github.com/vadikmash">GitHub</a></li>
			<li><a href="https://linedin.com/in/vadikmash">LinkedIn</a></li>
			<li><a href="https://x.com/vadikmash">X (Twitter)</a></li>
		</ul>
	</div>

	<h2>Tech Projects</h2>

	<h2>Music</h2>

	<h2>Wanna hire me? Check out my CV</h2>

</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
