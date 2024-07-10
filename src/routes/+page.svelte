<script lang="ts">
	import Menu from 'lucide-svelte/icons/menu';
	import Package2 from 'lucide-svelte/icons/package-2';
	import { Button } from '$lib/components/ui/button/index';
	import * as Sheet from '$lib/components/ui/sheet/index';
</script>

<div class="flex min-h-screen w-full flex-col">
	<header class="sticky top-0 flex h-16 items-center gap-4 bg-background px-4 md:px-6">
		<nav
			class="hidden w-full flex-col justify-around gap-6 text-lg font-medium md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
		>
			<div>
				<a href="##" class="flex items-center gap-2 text-lg font-semibold md:text-base">
					<img src="/main.png" width="32" height="32" alt="" />
				</a>
			</div>
			<div class="flex items-center gap-6">
				<!-- Adjusted here -->
				<a href="##" class="mx-1 text-white transition-colors">Main</a>
				<a href="##" class="mx-1 text-white transition-colors">Aquin 2.5</a>
				<a href="##" class="mx-1 text-white transition-colors">How</a>
				<a href="##" class="mx-1 text-white transition-colors">Soon</a>
				<a href="##" class="mx-1 text-white transition-colors">Forms</a>
				<a href="##" class="mx-1 text-white transition-colors">Install</a>
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
					<Package2 class="mb-6 h-6 w-6 text-white" />
					<!-- Added margin-bottom here -->
					<a href="##" class="text-white hover:text-foreground"> Dashboard </a>
					<a href="##" class="text-white hover:text-foreground"> Orders </a>
					<a href="##" class="text-white hover:text-foreground"> Products </a>
					<a href="##" class="text-white hover:text-foreground"> Customers </a>
					<a href="##" class="hover:text-foreground"> Settings </a>
				</nav>
			</Sheet.Content>
		</Sheet.Root>
	</header>
</div>
