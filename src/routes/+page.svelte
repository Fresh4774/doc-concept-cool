<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';

	import { onMount } from 'svelte';
	import Swiper from 'swiper';

	import { Autoplay, Navigation, Pagination } from 'swiper/modules';

	import 'swiper/css';
	import 'swiper/css/navigation';
	import 'swiper/css/pagination';

	let swiper;

	onMount(() => {
		swiper = new Swiper('.mySwiper', {
			spaceBetween: 2,
			centeredSlides: true,
			autoplay: {
				delay: 3000,
				disableOnInteraction: false
			},
			pagination: {
				el: '.swiper-pagination',
				clickable: true
			},
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev'
			},
			modules: [Autoplay, Navigation, Pagination]
		});
	});
</script>

<div class="flex min-h-screen w-full flex-col justify-center">
	<Navbar active="home" />
	<div class="flex items-center justify-center">
		<div class="swiper mySwiper">
			<div class="swiper-wrapper">
				<div class="swiper-slide">
					<main id="main1">
						<div>
							<h1 class="mb-4 text-center text-9xl font-bold max-sm:text-7xl">Aquin 2.5</h1>
							<div>
								<p class="paragraph-width text-center">
									Discover Aquin 2.5—a leap forward in innovation and user-friendliness. With
									cutting-edge updates and seamless functionality, Aquin 2.5 empowers you to achieve
									more. Explore now and experience the future of productivity!
								</p>
							</div>
							<br />
							<div class="flex justify-center gap-4">
								<a
									href="/"
									class="rounded-[30px] bg-[#fff] p-2 px-7 text-center text-lg text-[#000] transition-colors"
									>Login</a
								>
								<a
									href="https://youtube.com"
									target="_blank"
									class="rounded-[30px] bg-[#fff] p-2 px-7 text-center text-lg text-[#000] transition-colors"
									>Trailer</a
								>
							</div>
						</div>
					</main>
				</div>
				<div class="swiper-slide">
					<main id="main2">
						<div>
							<div id="video-container" class="relative overflow-hidden max-sm:w-full">
								<video autoplay muted loop class="h-full w-full object-cover">
									<source src="/main2.mp4" type="video/mp4" class="video" />
									Your browser does not support the video tag.
								</video>
							</div>
						</div>
					</main>
				</div>
				<div class="swiper-slide">
					<main id="main3">
						<div>
							<h1 class="mb-4 text-center text-9xl font-bold max-sm:text-7xl">AquinAi</h1>
							<div>
								<p class="paragraph-width text-center">
									AquinAI is your ultimate personal assistant, designed for efficiency and ease.
									With fast performance, robust security, and a friendly interface, AquinAI will
									assist you with all your tasks. We're excited to announce that AquinAI is in
									development and coming soon. Stay tuned!
								</p>
							</div>
							<br />
							<div>
								<div class="flex justify-center gap-4">
									<a
										href="/aquinai"
										class="rounded-[30px] bg-[#fff] p-2 px-10 text-center text-lg text-[#000] transition-colors"
										>Learn more</a
									>
								</div>
							</div>
						</div>
					</main>
				</div>

				<div class="swiper-slide">
					<main id="main4">
						<div class="items-center justify-center">
							<h1 class="mb-4 flex items-center text-center text-9xl font-bold max-sm:text-6xl">
								<svg
									clip-rule="evenodd"
									width="150"
									height="150"
									fill="#fff"
									fill-rule="evenodd"
									stroke-linejoin="round"
									stroke-miterlimit="2"
									viewBox="0 0 24 24"
									xmlns="http://www.w3.org/2000/svg"
									class="max-sm:w-20"
									><path
										d="m2.095 19.886 9.248-16.5c.133-.237.384-.384.657-.384.272 0 .524.147.656.384l9.248 16.5c.064.115.096.241.096.367 0 .385-.309.749-.752.749h-18.496c-.44 0-.752-.36-.752-.749 0-.126.031-.252.095-.367zm9.907-6.881c-.414 0-.75.336-.75.75v3.5c0 .414.336.75.75.75s.75-.336.75-.75v-3.5c0-.414-.336-.75-.75-.75zm-.002-3c-.552 0-1 .448-1 1s.448 1 1 1 1-.448 1-1-.448-1-1-1z"
										fill-rule="nonzero"
									/></svg
								>
								Downtime
							</h1>
						</div>
					</main>
				</div>
			</div>
			<div class="swiper-button-next"></div>
			<div class="swiper-button-prev"></div>
			<div class="swiper-pagination"></div>
		</div>
	</div>
	<Footer active="app" />
</div>
