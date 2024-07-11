<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="app" />
	<main class="my-5">
		<h1 class="text-center text-9xl font-bold">Aquin.</h1>
		<h2 class="my-6 text-center text-5xl">
			Something <span class="font-bold">Cool</span> +
			<span class="italic">Insane </span>
		</h2>
		<h3 class="text-center text-3xl font-medium">
			Get <span class="italic">answers</span> to the <span class="font-bold">questions</span> like never
			before!
		</h3>
	</main>
	<Footer active="app" />
</div>
