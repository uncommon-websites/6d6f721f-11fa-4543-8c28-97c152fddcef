<!--
    @component
    A call-to-action component that attracts attention and encourages user engagement.

    Usage:
    ```html
    <CallToAction
      title="Get started today"
      subtitle="Join now"
      description="Ready to experience the difference? Join our community of satisfied customers and see how our solution can transform your workflow."
      image="https://www.unc.mn/image-placeholder.svg"
      callsToAction={[
        {
          href: "/get-started",
          label: "Get Started",
          variant: "primary"
        },
        {
          href: "/contact",
          label: "Talk to Sales",
          variant: "secondary"
        }
      ]}
    />
    ```

    Props:
    - `title`: The main heading text (string)
    - `subtitle`: Secondary heading text (string)
    - `description`: Detailed information about the offer (string)
    - `callsToAction`: Array of CTA objects with href, label, and optional variant properties (CTA[])
    - `imageSrc`: portrait of the company's customer smiling at the camera.
-->

<script lang="ts">
	// Types
	import type { ComponentProps } from "svelte";

	// Components
	import Button from "../ui/Button.svelte";
	import AnimateText from "../animation/AnimateText.svelte";
	import { cta } from "$lib/navigation";

	// Types
	type CTA = {
		href: string;
		label: string;
		variant?: ComponentProps<typeof Button>["variant"];
	};

	// Props
	const {
		title = "Start your next big idea on a canvas built for it",
		subtitle = "Go from idea to execution—faster and clearer",
		description = "No logins, no waiting. Try the canvas and see what creative flow actually feels like with AI alongside you—not in the way. Stop juggling prompts, tabs, and timelines. Canvas AI gives you one infinite canvas to think, write, and iterate with AI—your way.",
		imageSrc = "/generated/image-candid-photo-of-a-creative-professional-.webp",
		callsToAction = [
			{
				href: "/get-started",
				label: "Try Canvas now",
				variant: "primary"
			},
			{
				href: "/contact",
				label: "Schedule demo",
				variant: "secondary"
			}
		],
		...rest
	}: {
		title?: string;
		subtitle?: string;
		description?: string;
		imageSrc?: string;
		callsToAction?: CTA[];
		[key: string]: any;
	} = $props();
</script>

<div class="" {...rest}>
	<section class="section-px section-py container mx-auto">
		<div
			class="bg-card border-border grid content-start items-center justify-between gap-(--gap) rounded-(--radius) border p-(--gap) text-balance [--gap:--spacing(8)] [--inner-radius:calc(var(--radius)-var(--gap))] [--radius:var(--radius-xl)] lg:grid-cols-[2fr_1fr]"
		>
			<div class="items-between grid h-full content-between gap-16">
				<h2 class="text-title1 mb-3 flex flex-col">
					<span><AnimateText text={title} /></span>
					<span class="text-emphasis-low"><AnimateText text={subtitle} /></span>
				</h2>
				<div class="flex flex-col items-start justify-start gap-7">
					<p class="text-headline text-emphasis-low">
						{description}
					</p>
					<div class="flex w-full flex-col gap-2 md:flex-row md:flex-wrap">
						{#each callsToAction as cta}
							<Button class="w-full md:w-auto" href={cta.href} variant={cta.variant || "primary"}
								>{cta.label}</Button
							>
						{/each}
					</div>
				</div>
			</div>
			<img
				src={imageSrc}
				alt="Creative professional confidently working on campaigns in modern agency workspace"
				class="hidden aspect-[4/5] size-full max-h-full w-full rounded-[calc(max(var(--inner-radius),.25rem))] object-cover lg:block"
			/>
		</div>
	</section>
</div>
