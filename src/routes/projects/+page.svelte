<script lang="ts">
	import { resolve } from '$app/paths';
	import MiniCarousel from '$lib/components/MiniCarousel.svelte';

	const projects = [
		{
			slug: '/dashboard',
			label: 'Marketing',
			title: 'Marketing Performance Dashboard',
			background: 'Analyzes 9,900 advertising records for a UK retail brand across Facebook, Instagram, and Pinterest. Tracking 19 distinct data fields — from social engagement to financial metrics — to identify peak spend efficiency.',
			tags: ['Facebook', 'Instagram', 'Pinterest', '9,900 Records'],
			slides: [
				{ src: '/overview.png',  label: 'Overview' },
				{ src: '/campaign.png',  label: 'Campaign' },
				{ src: '/channel.png',   label: 'Channel'  },
				{ src: '/city.png',      label: 'City'     },
			],
		},
		// Add more projects here
	];
</script>

<svelte:head>
	<title>Projects · Thy Tran</title>
</svelte:head>

<div class="max-w-6xl mx-auto px-6 sm:px-10 pt-16 pb-24">

	<a href={resolve('/')} class="text-sm font-sans text-base-content/40 hover:text-primary transition-colors">
		← Back
	</a>

	<div class="mt-10 mb-14">
		<p class="text-sm font-sans font-medium text-primary uppercase tracking-widest mb-3">
			Work
		</p>
		<h1 class="font-display text-6xl font-bold leading-tight">
			Projects
		</h1>
		<div class="w-12 h-px bg-primary mt-8"></div>
	</div>

	<div class="flex flex-col gap-12">
		{#each projects as project}
			<div class="card bg-base-200 shadow-md overflow-hidden">
				<div class="card-body p-0">
					<div class="grid grid-cols-1 lg:grid-cols-2 gap-0">

						<!-- Left: text -->
						<div class="p-8 lg:p-10 flex flex-col justify-between gap-6">
							<div>
								<span class="badge badge-primary badge-soft mb-4">{project.label}</span>
								<h2 class="font-display text-3xl font-bold leading-snug mb-4">{project.title}</h2>
								<p class="font-sans text-base-content/70 text-base leading-relaxed">{project.background}</p>
							</div>

							<div class="flex flex-col gap-4">
								<div class="flex flex-wrap gap-2">
									{#each project.tags as tag}
										<span class="badge badge-soft badge-info">{tag}</span>
									{/each}
								</div>
								<a href={resolve(project.slug as Parameters<typeof resolve>[0])} class="btn btn-primary w-fit font-normal text-sm">
									View Project →
								</a>
							</div>
						</div>

						<!-- Right: carousel -->
						<div class="p-6 lg:p-8 flex flex-col justify-center bg-base-300/40">
							<MiniCarousel slides={project.slides} />
						</div>

					</div>
				</div>
			</div>
		{/each}
	</div>

</div>
