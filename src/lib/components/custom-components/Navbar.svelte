<script lang="ts">
	import Menu from 'lucide-svelte/icons/menu';
	import { Button } from '$lib/components/ui/button/index';
	import * as Sheet from '$lib/components/ui/sheet/index';
	export let active;
</script>

<div class="top-0 mb-2 flex h-16 items-center gap-2 bg-background px-2">
	<nav
		class="hidden w-full flex-col items-center justify-around gap-6 text-lg font-medium md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
	>
		<div>
			<a href="/" class="flex items-center gap-2 text-lg font-semibold md:text-base">
				<img src="/main.png" width="32" height="32" alt="Aquin logo" />
			</a>
		</div>
		<div class="flex items-center gap-6">
			<!-- Adjusted here -->

			<a
				href="/"
				class="mx-1 font-bold {active === 'home'
					? 'text-[#3887BE] underline'
					: ''} transition-colors">AquinHub</a
			>
			<a
				href="/app"
				class="mx-1 font-bold {active === 'app'
					? 'text-[#3887BE] underline'
					: ''} transition-colors">App</a
			>
			<a
				href="/aquinai"
				class="mx-1 font-bold {active === 'aquinai'
					? 'text-[#3887BE] underline'
					: ''} transition-colors">AquinAi</a
			>
			<a
				href="/aquinpi"
				class="mx-1 font-bold {active === 'aquinpi'
					? 'text-[#3887BE] underline'
					: ''} transition-colors">AquinPi</a
			>
		</div>

		<div>
			<a
				href="/"
				class="rounded-md bg-[#3887BE] p-2 px-4 text-sm font-bold text-white transition-colors"
				>Login</a
			>
		</div>
	</nav>
	<Sheet.Root>
		<Sheet.Trigger asChild let:builder>
			<Button
				variant="outline"
				size="icon"
				class="shrink-0 align-baseline md:hidden"
				builders={[builder]}
			>
				<Menu class="h-5 w-5" />
				<span class="sr-only">Toggle navigation menu</span>
			</Button>
		</Sheet.Trigger>
		<Sheet.Content side="left">
			<nav class="grid gap-6 text-lg font-medium">
				<!-- <Package2 class="mb-6 h-6 w-6 text-white" /> -->
				<img src="/main.png" width="32" height="32" alt="Aquin logo" />
				<a href="##" class="mx-1 text-white transition-colors">AquinHub</a>
				<a href="##" class="mx-1 text-white transition-colors">App</a>
				<a href="##" class="mx-1 text-white transition-colors">AquinAi</a>
				<a href="##" class="mx-1 text-white transition-colors">AquinPi</a>
			</nav>
		</Sheet.Content>
	</Sheet.Root>
</div>
