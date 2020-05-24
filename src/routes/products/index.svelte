<script>
	import data from './products.json';
    export let products = data.products;
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<svelte:head>
	<title>Products</title>
</svelte:head>

<h1>My products</h1>

<ul>
	{#each products as product}
		<!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->
		<li><a rel='prefetch' href='products/{product.slug}'>{product.title}</a></li>
	{/each}
</ul>