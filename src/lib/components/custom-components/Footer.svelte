<script lang="ts">
	export let active;
</script>
<div
	class="my-5 flex items-center gap-2 border-t-[1px] border-gray-700 bg-transparent px-2 sm:h-auto md:h-16"
>
	<div
		class="flex w-full flex-col items-center justify-around gap-6 text-lg font-medium max-[820px]:flex-col max-sm:mt-3 sm:mt-6 sm:flex-row sm:gap-5 sm:text-sm lg:gap-6"
		id="footer-container"
	>
		<div class="flex items-center justify-center gap-4">
			<a href="/" class="flex items-center gap-2 text-lg font-semibold md:text-base">
				<img src="/main.png" width="32" height="32" alt="Aquin logo" /> Aquin
			</a>
		</div>
		<div class="flex items-center justify-center gap-4 sm:w-auto">
			<a
				href="https://www.youtube.com/@AquinF03/featured"
				class="rounded-md p-2 px-4 text-sm font-bold text-[#fefefe] transition-colors"
				target="_blank"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="#fefefe"
					width="21"
					height="21"
					viewBox="0 0 50 50"
				>
					<path
						d="M 44.898438 14.5 C 44.5 12.300781 42.601563 10.699219 40.398438 10.199219 C 37.101563 9.5 31 9 24.398438 9 C 17.800781 9 11.601563 9.5 8.300781 10.199219 C 6.101563 10.699219 4.199219 12.199219 3.800781 14.5 C 3.398438 17 3 20.5 3 25 C 3 29.5 3.398438 33 3.898438 35.5 C 4.300781 37.699219 6.199219 39.300781 8.398438 39.800781 C 11.898438 40.5 17.898438 41 24.5 41 C 31.101563 41 37.101563 40.5 40.601563 39.800781 C 42.800781 39.300781 44.699219 37.800781 45.101563 35.5 C 45.5 33 46 29.398438 46.101563 25 C 45.898438 20.5 45.398438 17 44.898438 14.5 Z M 19 32 L 19 18 L 31.199219 25 Z"
					></path>
				</svg>
			</a>•
			<a
				href="https://x.com/AquinF03"
				class="rounded-md p-2 px-4 text-sm font-bold text-[#fefefe] transition-colors"
				target="_blank"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="#fefefe"
					width="21"
					height="21"
					viewBox="0 0 30 30"
				>
					<path
						d="M26.37,26l-8.795-12.822l0.015,0.012L25.52,4h-2.65l-6.46,7.48L11.28,4H4.33l8.211,11.971L12.54,15.97L3.88,26h2.65 l7.182-8.322L19.42,26H26.37z M10.23,6l12.34,18h-2.1L8.12,6H10.23z"
					></path>
				</svg>
			</a>•
			<a
				href="https://www.instagram.com/aquinf03/"
				class="rounded-md p-2 px-4 text-sm font-bold text-[#fefefe] transition-colors"
				target="_blank"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="#fefefe"
					width="21"
					height="21"
					viewBox="0 0 50 50"
				>
					<path
						d="M 16 3 C 8.8324839 3 3 8.8324839 3 16 L 3 34 C 3 41.167516 8.8324839 47 16 47 L 34 47 C 41.167516 47 47 41.167516 47 34 L 47 16 C 47 8.8324839 41.167516 3 34 3 L 16 3 z M 16 5 L 34 5 C 40.086484 5 45 9.9135161 45 16 L 45 34 C 45 40.086484 40.086484 45 34 45 L 16 45 C 9.9135161 45 5 40.086484 5 34 L 5 16 C 5 9.9135161 9.9135161 5 16 5 z M 37 11 A 2 2 0 0 0 35 13 A 2 2 0 0 0 37 15 A 2 2 0 0 0 39 13 A 2 2 0 0 0 37 11 z M 25 14 C 18.936712 14 14 18.936712 14 25 C 14 31.063288 18.936712 36 25 36 C 31.063288 36 36 31.063288 36 25 C 36 18.936712 31.063288 14 25 14 z M 25 16 C 29.982407 16 34 20.017593 34 25 C 34 29.982407 29.982407 34 25 34 C 20.017593 34 16 29.982407 16 25 C 16 20.017593 20.017593 16 25 16 z"
					></path>
				</svg>
			</a>•
			<a
				href="https://discord.com/invite/suhwwzuAaX"
				class="rounded-md p-2 px-4 text-sm font-bold text-[#fefefe] transition-colors"
				target="_blank"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="#fefefe"
					width="21"
					height="21"
					viewBox="0 0 50 50"
				>
					<path
						d="M 41.625 10.769531 C 37.644531 7.566406 31.347656 7.023438 31.078125 7.003906 C 30.660156 6.96875 30.261719 7.203125 30.089844 7.589844 C 30.074219 7.613281 29.9375 7.929688 29.785156 8.421875 C 32.417969 8.867188 35.652344 9.761719 38.578125 11.578125 C 39.046875 11.867188 39.191406 12.484375 38.902344 12.953125 C 38.710938 13.261719 38.386719 13.429688 38.050781 13.429688 C 37.871094 13.429688 37.6875 13.378906 37.523438 13.277344 C 32.492188 10.15625 26.210938 10 25 10 C 23.789063 10 17.503906 10.15625 12.476563 13.277344 C 12.007813 13.570313 11.390625 13.425781 11.101563 12.957031 C 10.808594 12.484375 10.953125 11.871094 11.421875 11.578125 C 14.347656 9.765625 17.582031 8.867188 20.214844 8.425781 C 20.0625 7.929688 19.925781 7.617188 19.914063 7.589844 C 19.738281 7.203125 19.34375 6.960938 18.921875 7.003906 C 18.652344 7.023438 12.355469 7.566406 8.320313 10.8125 C 6.214844 12.761719 2 24.152344 2 34 C 2 34.175781 2.046875 34.34375 2.132813 34.496094 C 5.039063 39.605469 12.972656 40.941406 14.78125 41 C 14.789063 41 14.800781 41 14.8125 41 C 15.132813 41 15.433594 40.847656 15.621094 40.589844 L 17.449219 38.074219 C 12.515625 36.800781 9.996094 34.636719 9.851563 34.507813 C 9.4375 34.144531 9.398438 33.511719 9.765625 33.097656 C 10.128906 32.683594 10.761719 32.644531 11.175781 33.007813 C 11.234375 33.0625 15.875 37 25 37 C 34.140625 37 38.78125 33.046875 38.828125 33.007813 C 39.242188 32.648438 39.871094 32.683594 40.238281 33.101563 C 40.601563 33.515625 40.5625 34.144531 40.148438 34.507813 C 40.003906 34.636719 37.484375 36.800781 32.550781 38.074219 L 34.378906 40.589844 C 34.566406 40.847656 34.867188 41 35.1875 41 C 35.199219 41 35.210938 41 35.21875 41 C 37.027344 40.941406 44.960938 39.605469 47.867188 34.496094 C 47.953125 34.34375 48 34.175781 48 34 C 48 24.152344 43.785156 12.761719 41.625 10.769531 Z M 18.5 30 C 16.566406 30 15 28.210938 15 26 C 15 23.789063 16.566406 22 18.5 22 C 20.433594 22 22 23.789063 22 26 C 22 28.210938 20.433594 30 18.5 30 Z M 31.5 30 C 29.566406 30 28 28.210938 28 26 C 28 23.789063 29.566406 22 31.5 22 C 33.433594 22 35 23.789063 35 26 C 35 28.210938 33.433594 30 31.5 30 Z"
					></path>
				</svg>
			</a>
		</div>
		<div class="flex flex-col items-center justify-center gap-1 sm:w-auto sm:flex-row sm:gap-6">
			<a
				href="/tc"
				class="mx-1 flex font-bold {active === 'tc'
					? 'text-[#3887BE] underline'
					: ''} transition-colors"
			>
				Terms & Conditions
			</a>
			•
			<a
				href="/pp"
				class="mx-1 flex font-bold {active === 'pp'
					? 'text-[#3887BE] underline'
					: ''} transition-colors"
			>
				Privacy Policy
			</a>
			•
			<a
				href="/cp"
				class="mx-1 flex font-bold {active === 'cp'
					? 'text-[#3887BE] underline'
					: ''} transition-colors"
			>
				Cookie Policy
			</a>
			•
			<a
				href="/cp"
				class="mx-1 flex font-bold {active === 'cp'
					? 'text-[#3887BE] underline'
					: ''} transition-colors"
			>
				Aquin © 2023–2024
			</a>
		</div>
	</div>
</div>

<style>
	#footer-container {
		@media screen and (max-width: 820px) {
			margin-top: 10vh;
			flex-direction: column;
		}
	}
</style>
