<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>


<div class="flex min-h-screen w-full flex-col">
	<Navbar active="aquinai" />
	<main class="flex w-full justify-center items-center">
		<main id="main3">
			<div>
				<h1 class="mb-4 text-center text-9xl font-bold">AquinAi</h1>
				<div>
					<p class="text-center paragraph-width">
						AquinAI is your ultimate personal assistant, designed for efficiency and ease. With fast performance, robust security, and a friendly interface, AquinAI will assist you with all your tasks. We're excited to announce that AquinAI is in development and coming soon. Stay tuned!
					</p>
				</div>	
				<br />
				<div>
					<div class="flex justify-center gap-4">
						<a href="/aquinai" class="rounded-[30px] bg-[#fff] p-2 px-10 text-lg text-center text-[#000] transition-colors">More information coming soon...</a>
					</div>
				</div>
			</div>
		</main>
	</main>
	<Footer active="app" />
</div>
