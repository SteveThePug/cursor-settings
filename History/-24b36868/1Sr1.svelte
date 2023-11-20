<script>
	import Three from './Three.svelte';
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Three class=".three_container"/>
</section>

<style>
	three_container {
		width: 30vw;
	}
</style>
