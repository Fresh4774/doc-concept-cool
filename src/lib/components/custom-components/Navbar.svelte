<script lang="ts">
	import { onMount } from 'svelte';
	import Menu from 'lucide-svelte/icons/menu';
	import { Button } from '$lib/components/ui/button/index';
	import * as Sheet from '$lib/components/ui/sheet/index';

	export let active;

	onMount(() => {
		let musicButtons = document.querySelectorAll('.music-button');
		let audio = document.getElementById('audio') as HTMLAudioElement;

		musicButtons.forEach((musicButton) => {
			musicButton.addEventListener('click', () => {
				if (audio.paused) {
					audio.play();
					updatePlayState(true);
				} else {
					audio.pause();
					updatePlayState(false);
				}
			});
		});

		function updatePlayState(isPlaying: boolean) {
			let playIcons = document.querySelectorAll('.playIcon');
			let stopIcons = document.querySelectorAll('.stopIcon');

			playIcons.forEach((playIcon) => {
				(playIcon as HTMLElement).style.display = isPlaying ? 'none' : 'flex';
			});

			stopIcons.forEach((stopIcon) => {
				(stopIcon as HTMLElement).style.display = isPlaying ? 'flex' : 'none';
			});
		}
	});
</script>

<div class="top-0 flex h-16 items-center gap-2 bg-transparent px-2">
	<Sheet.Root>
		<Sheet.Trigger asChild let:builder class="flex items-center justify-center">
			<a href="/" class="flex items-center justify-center md:hidden">
				<img src="/main.png" width="65" height="65" alt="Aquin logo" />
			</a>
			<div class="w-[100%] md:hidden" />

			<div class="flex flex-row items-center md:hidden">
				<button class="music-button" id="musicButton">
					<svg
						class="playIcon"
						width="24"
						height="24"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 32 32"
					>
						<path
							fill="#fefefe"
							d="M15.5 4C9.149 4 4 9.149 4 15.5V18h7a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H6.5A4.5 4.5 0 0 1 2 25.5v-10C2 8.044 8.044 2 15.5 2S29 8.044 29 15.5v10a4.5 4.5 0 0 1-4.5 4.5H20a1 1 0 0 1-1-1V19a1 1 0 0 1 1-1h7v-2.5C27 9.149 21.851 4 15.5 4"
						/>
					</svg>
					<svg
						class="stopIcon"
						width="24"
						height="24"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 24 24"
						style="display: none;"
					>
						<path
							fill="#fefefe"
							d="M12 1a9 9 0 0 1 9 9v7c0 .62-.19 1.19-.5 1.67L15 13.18V12h4v-2a7 7 0 0 0-7-7c-2 0-3.77.82-5.04 2.14L5.55 3.72A8.96 8.96 0 0 1 12 1M2.78 3.5L20.5 21.22l-1.27 1.28l-2.5-2.5H15v-1.73l-6-6V20H6a3 3 0 0 1-3-3v-7c0-1.11.2-2.18.57-3.16L1.5 4.77zm2.39 4.94C5.06 8.94 5 9.46 5 10v2h3.73z"
						/>
					</svg>
				</button>
				<audio id="audio" src="/music.mp3"></audio>

				<a
					href="https://app.aquin.app"
					class="flex items-center text-sm font-bold text-[#fefefe] transition-colors"
				>
					Login
				</a>
			</div>

			<Button size="icon" class="shrink-0 align-baseline md:hidden" builders={[builder]}>
				<Menu class="h-5 w-5" />
				<span class="sr-only">Menu</span>
			</Button>
		</Sheet.Trigger>
		<Sheet.Content side="top" class="nav">
			<nav class="grid gap-4 text-lg font-medium">
				<img src="/main.png" width="32" height="32" alt="Aquin logo" />
				<a href="/" class="mx-1 text-[#fefefe] transition-colors">AquinHub</a>
				<a href="/app" class="mx-1 text-[#fefefe] transition-colors">App</a>
				<a href="/aquinai" class="mx-1 text-[#fefefe] transition-colors">AquinAi</a>
				<a href="/aquinpi" class="mx-1 text-[#fefefe] transition-colors">AquinPi</a>
			</nav>
		</Sheet.Content>
	</Sheet.Root>
	<nav
		class="hidden w-full flex-col items-center justify-around gap-6 text-lg font-medium md:flex md:flex-row md:gap-5 md:text-sm lg:gap-6"
	>
		<div>
			<a href="/" class="flex items-center gap-2 text-lg font-semibold md:text-base">
				<img src="/main.png" width="32" height="32" alt="Aquin logo" />
			</a>
		</div>
		<div class="flex items-center gap-6">
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

		<div class="flex flex-row items-center">
			<button class="music-button" id="musicButton">
				<svg
					class="playIcon"
					width="24"
					height="24"
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 32 32"
				>
					<path
						fill="#fefefe"
						d="M15.5 4C9.149 4 4 9.149 4 15.5V18h7a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H6.5A4.5 4.5 0 0 1 2 25.5v-10C2 8.044 8.044 2 15.5 2S29 8.044 29 15.5v10a4.5 4.5 0 0 1-4.5 4.5H20a1 1 0 0 1-1-1V19a1 1 0 0 1 1-1h7v-2.5C27 9.149 21.851 4 15.5 4"
					/>
				</svg>
				<svg
					class="stopIcon"
					width="24"
					height="24"
					xmlns="http://www.w3.org/2000/svg"
					viewBox="0 0 24 24"
					style="display: none;"
				>
					<path
						fill="#fefefe"
						d="M12 1a9 9 0 0 1 9 9v7c0 .62-.19 1.19-.5 1.67L15 13.18V12h4v-2a7 7 0 0 0-7-7c-2 0-3.77.82-5.04 2.14L5.55 3.72A8.96 8.96 0 0 1 12 1M2.78 3.5L20.5 21.22l-1.27 1.28l-2.5-2.5H15v-1.73l-6-6V20H6a3 3 0 0 1-3-3v-7c0-1.11.2-2.18.57-3.16L1.5 4.77zm2.39 4.94C5.06 8.94 5 9.46 5 10v2h3.73z"
					/>
				</svg>
			</button>
			<audio id="audio" src="/music.mp3"></audio>

			<a
				href="https://app.aquin.app"
				class="flex items-center text-lg font-semibold text-[#fefefe] transition-colors"
			>
				Login
			</a>
		</div>
	</nav>
</div>
