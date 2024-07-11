<script lang="ts">
	import Menu from 'lucide-svelte/icons/menu';
	import { Button } from '$lib/components/ui/button/index';
	import * as Sheet from '$lib/components/ui/sheet/index';

	export let active;
</script>

<div class="border-t-[1px] border-gray-700 mt-5 flex h-16 items-center gap-2 bg-background px-2 mb-2">
	<div
		class="items-center w-full flex-col justify-around gap-6 text-lg font-medium md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
	>
		<div>
			<a href="/" class="flex items-center gap-2 text-lg font-semibold md:text-base">
				<img src="/main.png" width="32" height="32" alt="Aquin logo" /> Aquin
			</a>
		</div>
		<div class="flex items-center gap-4">
			<a href="/" class="rounded-md text-white text-sm font-bold px-4 p-2 transition-colors">YT</a>•
			<a href="/" class="rounded-md text-white text-sm font-bold px-4 p-2 transition-colors">X</a>•
			<a href="/" class="rounded-md text-white text-sm font-bold px-4 p-2 transition-colors">IG</a>•
			<a href="/" class="rounded-md text-white text-sm font-bold px-4 p-2 transition-colors">DC</a>
		</div>
		<div class="flex items-center gap-6">
			<a href="/tc" class="mx-1 font-bold {active === 'tc' ? 'text-[#3887BE] underline' : ''} transition-colors"
				>Terms & Conditions</a
			>•
			<a
				href="/pp"
				class="mx-1 font-bold {active === 'pp' ? 'text-[#3887BE] underline' : ''} transition-colors"
				>Privacy Policy</a
			>•
			<a
				href="/cp"
				class="mx-1 font-bold {active === 'cp' ? 'text-[#3887BE] underline' : ''} transition-colors"
				>Cookie Policy</a
			>
		</div>
	</div>
</div>
