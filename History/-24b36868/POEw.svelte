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
		width: 50vw;
	}
</style>
