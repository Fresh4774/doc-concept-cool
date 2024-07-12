<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
	import Appheader from '$lib/components/custom-components/Appheader.svelte';
	import AppContentSection from '$lib/components/custom-components/AppContentSection.svelte';
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="app" />
	<Appheader />
	<main class="flex h-[75vh] w-full items-center justify-center">
		<AppContentSection title="About" description="About Aquin" imgSrc="/slice-app.jpg" />
	</main>
	<Footer active="app" />
</div>
