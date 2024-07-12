<script lang="ts">
	import * as Menubar from '$lib/components/ui/menubar/index.js';
</script>

<Menubar.Root>
	<Menubar.Menu>
		<Menubar.Item on:click={() => (window.location.href = '/app#chat')}>Chat</Menubar.Item>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Item on:click={() => (window.location.href = '/app#image')}>Image</Menubar.Item>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Item on:click={() => (window.location.href = '/app#call')}>Voice</Menubar.Item>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Item on:click={() => (window.location.href = '/app#pi')}>Pi</Menubar.Item>
	</Menubar.Menu>
</Menubar.Root>
