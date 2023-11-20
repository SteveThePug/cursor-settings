<script>
	import Three from './Three.svelte';
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Three></Three>
</section>

<style>
	Three {
		width: 30vw;
		height: 30vh;
	}
</style>
