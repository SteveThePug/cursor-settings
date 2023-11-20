<script>
	import { page } from '$app/stores';
</script>

<header>
	<a class="header-left">SteveThePug</a>
	<nav class="header-right">
		<a href="routes/cv" class="header-link">CV</a>
		<img src="your-image.png" alt="Your Image" />
	</nav>


</header>

<style>
	.header-left {
		float: left;
	}
	
	.header-right {
		float: right;
	}
	
	.header-link {
		margin-left: 10px;
		color: red;
		font-family: 'Inter', sans-serif;
		font-variation-settings: 'wght' 400;
		transition: font-variation-settings 0.3s ease;
	}
</style>