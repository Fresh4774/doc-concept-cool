<script lang="ts">
	import * as Menubar from '$lib/components/ui/menubar/index.js';

	// Function to scroll to the section with the given ID
	function scrollToSection(sectionId: string) {
		const sectionElement = document.getElementById(sectionId);
		if (sectionElement) {
			sectionElement.scrollIntoView({ behavior: 'smooth' });
		}
	}
</script>

<Menubar.Root>
	<Menubar.Menu>
		<Menubar.Item on:click={() => scrollToSection('aichat')}>Chat</Menubar.Item>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Item on:click={() => scrollToSection('aiimage')}>Image</Menubar.Item>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Item on:click={() => scrollToSection('aivoice')}>Voice</Menubar.Item>
	</Menubar.Menu>
	<!-- <Menubar.Menu>
		<Menubar.Item on:click={() => scrollToSection('aquinpi')}>Pi</Menubar.Item>
	</Menubar.Menu> -->
</Menubar.Root>
