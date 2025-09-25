<!--
@component AboutTeaser
A minimalist teaser for the about page.
-->
<script lang="ts">
	// Types
	type TeamMember = {
		name: string;
		role: string;
		image: string;
	};

	// Components
	import Button from "../ui/Button.svelte";
	import ScrollText from "./sub/ScrollText.svelte";

	// State
	let sectionRef: HTMLElement;

	let props = $props();

	// Data
	const teamMember: TeamMember = {
		name: "Sarah Chen",
		role: "Founder & CEO",
		image: "/generated/image-professional-founder-headshot-confident-.webp"
	};
</script>

<section bind:this={sectionRef} {...props}>
	<div class="section-px section-py container mx-auto">
		<div class="relative mx-auto grid max-w-4xl place-items-center gap-16">
			<ScrollText
				class="text-title1 text-center max-w-3xl"
				text={`"I spent three years watching brilliant copywriters burn out from tool fatigue. They'd create magic in their minds, then lose it juggling between fragmented AI apps. Canvas AI started as my midnight obsession to preserve that creative flow—because the best ideas shouldn't die in the gaps between tools."`}
			/>

			<!-- Team Member & CTA Section -->
			<div class="grid items-center gap-8">
				<div class="flex items-center justify-center gap-6">
					<img
						src={teamMember.image}
						alt={teamMember.name}
						class="size-16 rounded-full object-cover shadow-sm"
					/>
					<div class="flex flex-col items-start">
						<div class="text-callout font-medium">{teamMember.name}</div>
						<div class="text-caption text-emphasis-low mb-3">{teamMember.role}</div>
						<Button href="/about" variant="secondary" size="sm">Our story</Button>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
