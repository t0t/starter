<script>
	import data from './blog.json';
    export let posts = data.posts;
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<h1>Sidenav</h1>

<ul>
	{#each posts as post}
		<li><a rel='prefetch' href='blog/{post.slug}'>{post.title}</a></li>
	{/each}
</ul>