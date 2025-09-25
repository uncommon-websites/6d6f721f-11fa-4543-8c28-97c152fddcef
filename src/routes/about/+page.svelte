<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Creative-first thinking",
			description: "We believe creativity shouldn't be constrained by linear tools. Our infinite canvas approach lets ideas flow naturally, preserving the creative process that makes great work possible."
		},
		{
			title: "Uninterrupted flow",
			description: "Traditional AI tools break creative momentum with fragmented workflows. We've reimagined LLM interaction through spatial design, so you never lose your train of thought."
		},
		{
			title: "Your voice, amplified",
			description: "AI should enhance your unique creative voice, not replace it. Our multi-thread conversations adapt to your brand and tone while keeping you in creative control."
		}
	];
</script>

<SecondaryHero
	title="Where AI meets your ideas"
	subtitle="Creative thinking, uninterrupted"
	imageSrc="/generated/image-creative-team-collaborating-on-an-innova.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We began with a simple observation: creative minds don't think in linear chat bubbles. Every agency we visited had the same story—brilliant creatives switching between dozens of tabs, losing ideas in prompt histories, and fighting AI tools that worked against their natural process.",
		"The solution wasn't another AI chatbot. It was reimagining how humans and AI collaborate in the first place. We created an infinite canvas where ideas can breathe, expand, and connect—just like they do in your mind.",
		"Today, creative teams at agencies worldwide use Canvas AI to transform complex campaigns from scattered chaos into organized creative flows. No more fragmented workflows. No more lost momentum.",
		"We believe creativity deserves better tools. Tools that adapt to your process, preserve your voice, and amplify your ideas without getting in the way. That's the Canvas AI difference."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- Team and investor sections removed - no company information available -->

<!-- CTA Section -->
<CallToAction
	title="Transform your creative workflow"
	subtitle="From fragmented tools to infinite possibilities"
	description="Join creative professionals at leading agencies who've discovered what happens when AI finally works the way your mind does. Stop juggling tabs, prompts, and timelines. Start creating on a canvas built for your ideas."
/>
