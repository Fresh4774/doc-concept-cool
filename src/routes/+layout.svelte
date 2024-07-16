<script>
	import '../app.css';
	export let children;
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>

<div class="bg-[#000000] text-primary-foreground">
	<Navbar active={null} />
	<slot></slot>
	<Footer active={null} />
</div>
