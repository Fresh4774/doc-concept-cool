<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="tc" />
	<main class="flex h-[75vh] w-full items-center justify-center">
		<h1 class="text-9xl font-bold">Cooking...</h1>
	</main>
	<Footer active="tc" />
</div>
