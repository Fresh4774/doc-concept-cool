<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>


<div class="flex min-h-screen w-full flex-col">
	<Navbar active="aquinai" />
	<main class="h-[75vh] flex w-full justify-center items-center">
		<h1 class="text-9xl font-bold">Cooking...</h1>
	</main>
	<Footer active="app" />
</div>
