<script>
	import { page } from '$app/stores';
</script>

<header>
	<a class="header-left">SteveThePug</a>
	<nav class="header-right">
		<a href="/cv" class="header-link">CV</a>
		<img src="svelte-welcome.png" alt="Your Image" />
	</nav>


</header>

<style>
	.header-left {
		float: left;
		padding: 10px;
	}
	
	.header-right {
		float: right;
		padding: 10px;
	}
	
	.header-link {
		margin-left: 10px;
		font-family: 'Inter', sans-serif;
		font-variation-settings: 'wght' 400;
		transition: font-variation-settings 0.3s ease;
		font-size: 18px;
	}
</style>