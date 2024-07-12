<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="aquinai" />
	<main class="flex w-full items-center justify-center">
		<main id="aquinai">
			<div>
				<h1 class="anitxt mb-4 text-center text-9xl font-bold max-sm:text-5xl">AquinAi</h1>
				<div>
					<p class="paragraph-width text-center">
						AquinAI is your ultimate personal assistant, designed for efficiency and ease. With fast
						performance, robust security, and a friendly interface, AquinAI will assist you with all
						your tasks. We're excited to announce that AquinAI is in development and coming soon.
						Stay tuned!
					</p>
				</div>
				<br />
				<div>
					<div class="flex justify-center gap-4">
						<a
							href="/aquinai"
							class="rounded-[30px] bg-[#fff] p-2 px-10 text-center text-lg text-[#000] transition-colors"
							>More coming soon</a
						>
					</div>
				</div>
			</div>
		</main>
	</main>
	<Footer active="app" />
</div>
