<script lang="ts">
	import Navbar from '$lib/components/custom-components/Navbar.svelte';
	import Footer from '$lib/components/custom-components/Footer.svelte';
	import Appheader from '$lib/components/custom-components/Appheader.svelte';
	import AppContentSection from '$lib/components/custom-components/AppContentSection.svelte';

	const features = [
		{
			title: 'AI Chat',
			description:
				'AI Chat, our advanced feature designed to enhance productivity and streamline communication. With natural, flowing conversations powered by cutting-edge AI, it understands context, responds accurately, and learns over time. Enjoy personalized assistance, robust language support, and seamless integration with other app features, making your tasks easier and more efficient. AI Chat provides reliable and responsive support whenever you need it. Explore smarter communication with AI Chat and achieve your goals effortlessly.',
			src: '/chat.png',
			isVideo: false,
			sectionId: 'aichat'
		},
		{
			title: 'AI Voice Call',
			description:
				'Our advanced feature designed to revolutionize communication. Enjoy natural, real-time conversations with cutting-edge AI that understands context and responds accurately. With robust language support, personalized assistance, and seamless integration with other app features, AI Voice Chat makes tasks easier and more efficient. It offers reliable and responsive support whenever you need it. Experience smarter, hands-free communication with AI Voice Chat and achieve your goals effortlessly.',
			src: '/call.png',
			isVideo: false,
			sectionId: 'aivoice'
		},
		{
			title: 'AI Image Generator',
			description:
				'Our innovative feature designed to bring your creative visions to life. With advanced AI algorithms, effortlessly generate high-quality images tailored to your needs. Whether for professional projects or personal use, AI Image Generation offers precise, customizable results. Seamlessly integrated with other app features, it enhances productivity and creativity. It provides reliable and responsive support whenever you need it. Discover the future of visual creation with AI Image Generation and transform your ideas into stunning images effortlessly.',
			src: '/slice-app.jpg',
			isVideo: false,
			sectionId: 'aiimage'
		},
		{
			title: 'Utility Commands',
			description:
				'Our powerful feature designed to enhance your productivity and streamline tasks. Execute a wide range of commands efficiently, from managing files and data to automating routine processes. With intuitive controls and seamless integration with other app features, Utility Commands simplify complex tasks and boost efficiency. They offer reliable and responsive support whenever you need it. Experience the convenience and power of Utility Commands and achieve your goals effortlessly.',
			src: '/utility.png',
			isVideo: false,
			sectionId: 'utilitycommands'
		},
		// { title: 'Aquin Pi', description: '', src: '/chat.png', isVideo: false, sectionId: 'aquinpi' },
		{
			title: 'Research',
			description:
				'Here advanced AI empowers you to explore and synthesize information effortlessly. Generate multiple responses simultaneously and combine them seamlessly to enhance your research capabilities. Whether analyzing data, crafting insights, or generating diverse perspectives, our AI-driven research tool supports your quest for knowledge. Integrated with intuitive controls and designed for efficiency, it streamlines the research process, making it easier to extract meaningful insights. Experience the power of AI in research, provides reliable and responsive support. Embrace a smarter approach to research with our feature and uncover new possibilities effortlessly.',
			src: '/spr-motion.mp4',
			isVideo: true,
			sectionId: 'research'
		},
		{
			title: 'YouTube Summarizer',
			description:
				"A cutting-edge tool designed to streamline your video consumption experience. Simply provide a YouTube video link, and our AI-powered summarizer will analyze and condense the content into concise summaries. Whether you're researching, learning, or staying informed, our summarizer helps you extract key insights efficiently. Integrated seamlessly with intuitive controls, it enhances productivity by saving you time and effort. Our YouTube Summarizer offers reliable and responsive support whenever you need it. Explore a smarter way to digest YouTube content with our feature and stay ahead effortlessly.",
			src: '/yt-summarizer.png',
			isVideo: false,
			sectionId: 'yt-summarizer'
		}
	];
</script>

<div class="flex min-h-screen w-full flex-col">
	<Navbar active="app" />
	<Appheader />
	<main
		class="flex h-[75vh] w-full flex-1 flex-col items-center justify-center space-y-4 pb-16 pt-16"
	>
		{#each features as feature}
			<AppContentSection
				title={feature.title}
				description={feature.description}
				src={feature.src}
				isVideo={feature.isVideo}
				sectionId={feature.sectionId}
			/>
		{/each}
	</main>
	<Footer active="app" />
</div>
