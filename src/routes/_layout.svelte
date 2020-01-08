<script>
	import Nav from "../components/nav.svelte";

	export let segment;
</script>

<style>
	.section {
		padding: 1rem 1.5rem;
	}
</style>

<Nav {segment}/>

<div class="container">
	<div class="section content">
		<slot></slot>
	</div>
</div>
