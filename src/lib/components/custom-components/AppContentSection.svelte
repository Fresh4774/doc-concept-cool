<script lang="ts">
	export let title;
	export let description;
	export let imgSrc;
</script>

<div class="flex flex-col items-center justify-center p-4 lg:w-3/4 lg:flex-row lg:items-start">
	<div class="max-lg:order-2 max-lg:m-2 lg:mr-4 lg:w-2/4">
		<img src={imgSrc} alt="Main App" class="h-auto" />
	</div>
	<div class="max-lg:order-1 max-lg:mb-4 max-lg:text-center lg:ml-4 lg:w-2/4">
		<h2 class="mb-2 text-xl font-bold">{title}</h2>
		<p class="text-base">
			{description}
		</p>
	</div>
</div>
