<script lang="ts">
	import Check from 'lucide-svelte/icons/check';
	import ChevronsUpDown from 'lucide-svelte/icons/chevrons-up-down';
	import { tick } from 'svelte';
	import * as Command from '$lib/components/ui/command/index.js';
	import * as Popover from '$lib/components/ui/popover/index.js';
	import { Button } from '$lib/components/ui/button/index.js';
	import { cn } from '$lib/utils.js';

	const features = [
		{
			value: 'aichat',
			label: 'AI Chat'
		},
		{
			value: 'aivoicecall',
			label: 'AI Voice Call'
		},
		{
			value: 'aiimagegenerator',
			label: 'AI Image Generator'
		},
		{
			value: 'utilitycommands',
			label: 'Utility Commands'
		},
		{ value: 'aquinpi', label: 'Aquin Pi' },
		{
			value: 'research',
			label: 'Research'
		},
		{
			value: 'youtube-summarizer',
			label: 'YouTube Summarizer'
		},
		{
			value: 'accessibility',
			label: 'Accessibilty'
		}
	];

	let open = false;
	let value = '';

	$: selectedValue = features.find((f) => f.value === value)?.label ?? 'Search Features...';

	// We want to refocus the trigger button when the user selects
	// an item from the list so users can continue navigating the
	// rest of the form with the keyboard.
	function closeAndFocusTrigger(triggerId: string) {
		open = false;
		tick().then(() => {
			document.getElementById(triggerId)?.focus();
		});
	}
</script>

<Popover.Root bind:open let:ids>
	<Popover.Trigger asChild let:builder>
		<Button
			builders={[builder]}
			variant="outline"
			role="combobox"
			aria-expanded={open}
			class="w-[200px] justify-between"
		>
			{selectedValue}
			<ChevronsUpDown class="ml-2 h-4 w-4 shrink-0 opacity-50" />
		</Button>
	</Popover.Trigger>
	<Popover.Content class="w-[200px] p-0">
		<Command.Root class="bg-primary text-white">
			<Command.Input placeholder="Search features..." />
			<Command.Empty>No feature found.</Command.Empty>
			<Command.Group>
				{#each features as feature}
					<Command.Item
						value={feature.value}
						class="text-white"
						onSelect={(currentValue) => {
							value = currentValue;
							closeAndFocusTrigger(ids.trigger);
							window.location.href = `/app#${feature.value}`;
						}}
					>
						<Check class={cn('mr-2 h-4 w-4', value !== feature.value && 'text-transparent')} />
						{feature.label}
					</Command.Item>
				{/each}
			</Command.Group>
		</Command.Root>
	</Popover.Content>
</Popover.Root>
