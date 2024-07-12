<script>
	import AppSearchBar from '$lib/components/custom-components/AppSearchBar.svelte';
	import AppCategories from '$lib/components/custom-components/AppCategories.svelte';
</script>

<div class="top-0 mb-2 flex h-16 items-center gap-2 px-2">
	<div
		class="w-full flex-col items-center justify-around gap-6 text-lg font-medium max-sm:justify-center md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
	>
		<div class="flex max-w-sm items-center max-sm:my-3 max-sm:justify-center">
			<AppSearchBar />
		</div>
		<div class="flex max-w-sm items-center max-sm:my-3 max-sm:justify-center">
			<!-- <Appheader /> -->
			<AppCategories />
		</div>
	</div>
</div>
