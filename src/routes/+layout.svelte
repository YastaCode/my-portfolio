<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
  	import Footer from '$lib/skeleton/Footer.svelte';
	
	let { children } = $props();
	
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
</svelte:head>

<div class="skeleton">
	{@render children?.()}
	<Footer />
</div>
