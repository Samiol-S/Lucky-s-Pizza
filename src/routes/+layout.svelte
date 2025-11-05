<script>
	import favicon from '$lib/assets/favicon.webp';
	import { onMount } from 'svelte';
	import '../global.css';
	import Lenis from 'lenis';

	let { children } = $props();
	

	onMount(() => {
		const lenis = new Lenis({
			autoRaf: true,
		})
	})
	
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
