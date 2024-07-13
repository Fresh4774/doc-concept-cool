<script lang="ts">
	export let title;
	export let description;
	export let src;
	export let isVideo;
	export let sectionId;
</script>

<div
	id={sectionId}
	class="flex flex-col items-center justify-center p-4 lg:w-3/4 lg:flex-row lg:items-center"
>
	<div class="max-lg:order-2 max-lg:m-2 lg:mr-4 lg:w-2/4">
		{#if isVideo}
			<!-- svelte-ignore a11y-media-has-caption -->
			<video class="h-auto" autoplay loop>
				<source {src} type="video/mp4" />
				Your browser does not support the video tag.
			</video>
		{/if}
		{#if !isVideo}
			<img {src} alt={title} class="h-auto" />
		{/if}
	</div>
	<div class="max-lg:order-1 max-lg:mb-4 max-lg:text-center lg:ml-4 lg:w-2/4">
		<h2 class="mb-2 text-6xl font-bold max-sm:text-4xl">{title}</h2>
		<p class="text-base text-gray-400">
			{description}
		</p>
	</div>
</div>
