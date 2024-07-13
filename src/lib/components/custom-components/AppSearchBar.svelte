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
			value: 'AI Chat',
			section: 'aichat',
			label: 'AI Chat'
		},
		{
			value: 'AI Voice Call',
			section: 'aivoice',
			label: 'AI Voice Call'
		},
		{
			value: 'AI Image Generator',
			section: 'aiimage',
			label: 'AI Image Generator'
		},
		{
			value: 'Utility Commands',
			section: 'utilitycommands',
			label: 'Utility Commands'
		},
		// { value: 'Aquin Pi', section: 'aquinpi', label: 'Aquin Pi' },
		{
			value: 'Research',
			section: 'research',
			label: 'Research'
		},
		{
			value: 'YouTube Summarizer',
			section: 'yt-summarizer',
			label: 'YouTube Summarizer'
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

	// Function to scroll to the section with the given ID
	function scrollToSection(sectionId: string) {
		const sectionElement = document.getElementById(sectionId);
		if (sectionElement) {
			sectionElement.scrollIntoView({ behavior: 'smooth' });
		}
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
							scrollToSection(feature.section);
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
