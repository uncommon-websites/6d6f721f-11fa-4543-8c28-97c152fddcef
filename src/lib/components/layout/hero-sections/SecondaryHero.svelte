<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";

	let {
		title,
		subtitle,
		imageSrc = "https://www.unc.mn/image-placeholder.svg",
		...rest
	}: {
		title: string;
		subtitle: string;
		imageSrc: string;
		[key: string]: any;
	} = $props();
</script>

<header class={[
	"border-b border-border transition-colors duration-300",
	"bg-background"
]} {...rest}>
	<div class="section-px section-py container mx-auto">
		<div class={[
			"grid gap-12 lg:gap-16",
			"max-w-6xl mx-auto"
		]}>
			<div class="text-center space-y-4">
				<SectionHeader {title} {subtitle} size="lg" />
			</div>
			
			<div class={[
				"aspect-video overflow-hidden rounded-xl",
				"bg-muted/50 transition-all duration-500 ease-out",
				"hover:scale-[1.02] border border-border hover:border-primary/20",
				"group"
			]}>
				<img
					class={[
						"h-full w-full object-cover",
						"transition-transform duration-700 ease-out",
						"group-hover:scale-105"
					]}
					src={imageSrc}
					alt="Creative team collaborating in modern workspace"
					loading="lazy"
				/>
			</div>
		</div>
	</div>
</header>
