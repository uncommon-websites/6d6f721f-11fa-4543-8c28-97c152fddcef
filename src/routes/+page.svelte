<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Think across ideas. Not chat threads."
	subtitle="Work visually on campaigns with endless context."
	imageSrc="/generated/image-modern-creative-agency-in-a-sunlit-loft-.webp"
	centered={false}
/>
<LogoScroller 
	label="Trusted by creative teams at"
	logoUrls={[
		'https://cdn.brandfetch.io/ogilvy.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/wieden-kennedy.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/droga5.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/72andsunny.com/w/400/h/400/logo'
	]}
/>

<Summary
	generating
	title="What we do"
	text="Our technology delivers measurable results through secure, adaptable solutions that directly increase productivity and drive growth."
/>

<Testimonials
	testimonials={[
		{
			name: "Maria Esperanza Rodriguez",
			position: "Creative Director",
			company: "Momentum Agency",
			quote:
				"Canvas AI cut our campaign development time from 3 weeks to 5 days. We can now run parallel creative threads for different brand voices, saving us $40K per quarter in overtime costs while maintaining our signature creativity.",
			image: "/generated/image-professional-headshot-of-a-confident-lat.webp"
		},
		{
			name: "Kai Chen",
			position: "Senior Copywriter",
			company: "Bright Digital",
			quote:
				"Before Canvas AI, I was constantly losing context switching between 8 different tools. Now I manage 15 client campaigns simultaneously on one canvas, reducing my project turnaround by 60% and eliminating the risk of mixing up brand guidelines.",
			image: "/generated/image-professional-headshot-of-a-confident-asi.webp"
		},
		{
			name: "Zara Williams",
			position: "Content Strategy Lead",
			company: "Studio Collective",
			quote:
				"The infinite canvas approach eliminated our biggest pain point—fragmented creative workflows. We've recovered 20 hours per week that were lost to tool-switching, allowing our team to take on 40% more clients without burning out.",
			image: "/generated/image-professional-headshot-of-a-confident-bla.webp"
		}
	]}
/>

<Features
	generating
	title="Features"
	subtitle="Some features"
	features={[
		{
			title: "Streamlined Workflows",
			description:
				"Automate repetitive tasks and connect systems to improve productivity with our industry-leading 87% time savings."
		},
		{
			title: "Data Analysis",
			description:
				"Extract meaningful insights from your data with powerful analytical tools backed by proprietary AI algorithms that are 3x more accurate than competitors."
		},
		{
			title: "Secure Collaboration",
			description:
				"Work together seamlessly while maintaining strict data privacy standards with our zero-knowledge architecture and military-grade encryption."
		}
	]}
/>
<AboutTeaser generating />
<CallToAction generating />
