<script lang="ts">
	import { navIsOpen } from '$lib/store';
	import { fade, fly } from 'svelte/transition';
	import Lenis from '@studio-freight/lenis';

	// your script goes here
	import '../app.css';
	import { quadInOut } from 'svelte/easing';
	import { onMount } from 'svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Nav from '$lib/components/Nav.svelte';

	onMount(() => {
		const lenis = new Lenis();

		lenis.on('scroll', (e: any) => {});

		function raf(time: any) {
			lenis.raf(time);
			requestAnimationFrame(raf);
		}

		requestAnimationFrame(raf);
	});
</script>

<header>
	<Nav/>
</header>

<main>
	<slot />
</main>

<footer>
	<Footer/>
</footer>

<style>
	header {
		width: 100%;
		padding: 2rem 5vw;
	}

</style>
