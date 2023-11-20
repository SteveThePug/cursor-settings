<script>
	import Three from './Three.svelte';
	
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="three_container">
		<Three />
	</div>
</section>

<style>
	.three_container {
		justify-content: center;
		justify-self: center;
		width: 100vw;
		height: 10vh;
	}
</style>
