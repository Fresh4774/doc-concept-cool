<script>
	import AppSearchBar from '$lib/components/custom-components/AppSearchBar.svelte';
	import AppCategories from '$lib/components/custom-components/AppCategories.svelte';
</script>

<div
	class="top-0 mb-2 flex h-16 items-center gap-2 px-2 max-lg:mb-24 max-md:mb-12 max-md:justify-center"
>
	<div
		class="w-full flex-col items-center justify-around gap-6 text-lg font-medium max-sm:justify-center md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
	>
		<div class="mx-auto my-3 flex max-w-sm items-center justify-center">
			<AppSearchBar />
		</div>
		<div class="mx-auto my-3 flex max-w-sm items-center justify-center">
			<AppCategories />
		</div>
	</div>
</div>
