<style>
	@import url("https://unpkg.com/fluent-svelte/theme.css");
	:global(body) {
		background-color: var(--fds-solid-background-base);
		color: var(--fds-text-primary);
	}
</style>

<script>
	import { Router, Route, Link } from "svelte-navigator";
	import { TextBox , Button } from "fluent-svelte";
	import GradientText from 'svelte-gradient-typography';
	let value = "";
	import Blog from "./Blog.svelte";
</script>

<TextBox placeholder="Chose a Name" bind:value />

<Router>
    <nav>
			<Link to="blog">Blog</Link>
    </nav>

  <main>
    <Route path="/blog" component={Blog} />
  </main>
</Router>

<Button href="/blog"/>

<GradientText>
    The {value}
</GradientText>
