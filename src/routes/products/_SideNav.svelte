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

<ul>
	{#each products as product}
		<li><a rel='prefetch' href='products/{product.slug}'>{product.title}</a></li>
	{/each}
</ul>