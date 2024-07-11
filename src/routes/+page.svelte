<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="home" />
	<div class="swiper mySwiper">
		<div class="swiper-wrapper">
			<div class="swiper-slide">
				<main id="main1">
					<div>
						<h1 class="mb-4 text-center text-9xl font-bold">Aquin 2.5</h1>
						<p class="text-center">
							Aquin 2.5 has been released and it brought some really cool and big changes to the
							whole application
						</p>
						<br />
						<div>
							<a
								href="/"
								class="rounded-md bg-[#3887BE] p-2 px-4 text-sm font-bold text-white transition-colors"
								>Login</a
							>
						</div>
					</div>
				</main>
			</div>
			<div class="swiper-slide">
				<main id="main2">
					<div>
						<h1 class="mb-4 text-center text-9xl font-bold">Aquin 2.6</h1>
						<p class="text-center">
							Aquin 2.6 has been released and it brought some really cool and big changes to the
							whole application
						</p>
						<br />
						<div>
							<a
								href="/"
								class="rounded-md bg-[#3887BE] p-2 px-4 text-sm font-bold text-white transition-colors"
								>Login</a
							>
						</div>
					</div>
				</main>
			</div>
			<div class="swiper-slide">
				<main id="main3">
					<div>
						<h1 class="mb-4 text-center text-9xl font-bold">Aquin 2.7</h1>
						<p class="text-center">
							Aquin 2.7 has been released and it brought some really cool and big changes to the
							whole application
						</p>
						<br />
						<div>
							<a
								href="/"
								class="rounded-md bg-[#3887BE] p-2 px-4 text-sm font-bold text-white transition-colors"
								>Login</a
							>
						</div>
					</div>
				</main>
			</div>

			<div class="swiper-slide">
				<main id="main4">
					<div>
						<h1 class="mb-4 text-center text-9xl font-bold">Aquin 2.8</h1>
						<p class="text-center">
							Aquin 2.7 has been released and it brought some really cool and big changes to the
							whole application
						</p>
						<br />
						<div>
							<a
								href="/"
								class="rounded-md bg-[#3887BE] p-2 px-4 text-sm font-bold text-white transition-colors"
								>Login</a
							>
						</div>
					</div>
				</main>
			</div>
		</div>
		<div class="swiper-button-next"></div>
		<div class="swiper-button-prev"></div>
		<div class="swiper-pagination"></div>
	</div>

	<script>
		var swiper = new Swiper('.mySwiper', {
			spaceBetween: 2,
			centeredSlides: true,
			autoplay: {
				delay: 2000,
				disableOnInteraction: false
			},
			pagination: {
				el: '.swiper-pagination',
				clickable: true
			},
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev'
			}
		});
	</script>
	<Footer active="app" />
</div>
