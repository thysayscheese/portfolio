<script lang="ts">
	import { resolve, base } from '$app/paths';
	import MiniCarousel from '$lib/components/MiniCarousel.svelte';

	const slides = [
		{ src: `${base}/overview.png`,  label: 'Overview' },
		{ src: `${base}/campaign.png`,  label: 'Campaign' },
		{ src: `${base}/channel.png`,   label: 'Channel'  },
		{ src: `${base}/city.png`,      label: 'City'     },
	];
</script>

<svelte:head>
	<title>Marketing Dashboard · Thy Tran</title>
</svelte:head>

<div class="max-w-6xl mx-auto px-6 sm:px-10 pt-16 pb-24">

	<!-- Back -->
	<a href={resolve('/projects')} class="text-sm font-sans text-base-content/40 hover:text-primary transition-colors">
		← Back
	</a>

	<!-- Title (full width, above the grid) -->
	<div class="mt-10">
		<p class="text-sm font-sans font-medium text-primary uppercase tracking-widest mb-3">
			Project
		</p>

		<h1 class="font-display text-6xl font-bold leading-tight mb-4">
			Marketing<br />Dashboard
		</h1>

		<div class="w-12 h-px bg-primary mt-8 mb-10"></div>
	</div>

	<!-- Two-column: background left, carousel right — aligned from "Background" -->
	<div class="grid grid-cols-1 lg:grid-cols-2 gap-10 lg:gap-16 items-start">

		<!-- Left: background text + CTA -->
		<div>
			<h2 class="font-display text-xl font-semibold mb-4">Background</h2>

			<p class="font-sans text-base-content/75 text-lg leading-relaxed mb-8">
				This project analyzes 9,900 advertising records for a UK retail brand to evaluate performance across Facebook, Instagram, and Pinterest. By tracking 19 distinct data fields — ranging from social engagement to deep financial metrics — I built an end-to-end analysis to identify where the brand can achieve the highest <em>spend efficiency</em>.
			</p>

			<a href={resolve('/marketing-dashboard')} class="btn btn-primary text-sm font-normal">
				Open Dashboard →
			</a>
		</div>

		<!-- Right: carousel -->
		<div class="w-full">
			<MiniCarousel {slides} />
		</div>
	</div>

	<!-- Divider -->
	<div class="w-full h-px bg-base-200 my-16"></div>

	<!-- Key Insights -->
	<h2 class="font-display text-3xl font-bold mb-10">Key Insights</h2>

	<div class="grid grid-cols-1 sm:grid-cols-2 gap-6">

		<!-- 1 -->
		<div class="card bg-base-200 card-md">
			<div class="card-body gap-3">
				<div class="flex items-center gap-3">
					<span class="badge badge-primary badge-soft badge-lg">01</span>
					<h3 class="card-title font-display text-lg">Channel Efficiency: Pinterest is the ROI Champion</h3>
				</div>
				<p class="font-sans text-base-content/70 text-sm leading-relaxed">
					While Facebook often receives higher budgets due to higher engagement, the data shows that Pinterest is the most cost-effective channel.
				</p>
				<ul class="font-sans text-sm text-base-content/75 space-y-2 mt-1">
					<li class="flex gap-2"><span class="text-primary mt-0.5">▸</span><span><strong>ROI Leadership:</strong> Pinterest delivers an average ROI of 21.47, significantly outperforming Instagram (9.80) and Facebook (4.76).</span></li>
					<li class="flex gap-2"><span class="text-primary mt-0.5">▸</span><span><strong>Cost-Effectiveness:</strong> Pinterest has the lowest CPM at £6.47 — roughly 50% cheaper than Facebook (£13.17) for brand awareness.</span></li>
				</ul>
			</div>
		</div>

		<!-- 2 -->
		<div class="card bg-base-200 card-md">
			<div class="card-body gap-3">
				<div class="flex items-center gap-3">
					<span class="badge badge-secondary badge-soft badge-lg">02</span>
					<h3 class="card-title font-display text-lg">Device Performance: Desktop vs. Mobile</h3>
				</div>
				<p class="font-sans text-base-content/70 text-sm leading-relaxed">
					User behavior varies significantly by device, with Desktop users showing a higher intent to complete purchases.
				</p>
				<ul class="font-sans text-sm text-base-content/75 space-y-2 mt-1">
					<li class="flex gap-2"><span class="text-secondary mt-0.5">▸</span><span><strong>Higher Conversion:</strong> Desktop users achieved a CR of 23.99%, compared to 20.43% for Mobile users.</span></li>
					<li class="flex gap-2"><span class="text-secondary mt-0.5">▸</span><span><strong>City-Level Trends:</strong> Desktop consistently contributes a higher CR across London, Manchester, and Birmingham.</span></li>
				</ul>
			</div>
		</div>

		<!-- 3 -->
		<div class="card bg-base-200 card-md">
			<div class="card-body gap-3">
				<div class="flex items-center gap-3">
					<span class="badge badge-accent badge-soft badge-lg">03</span>
					<h3 class="card-title font-display text-lg">Creative Strategy: The Power of Discounts</h3>
				</div>
				<p class="font-sans text-base-content/70 text-sm leading-relaxed">
					The format of the advertisement plays a critical role in profitability.
				</p>
				<ul class="font-sans text-sm text-base-content/75 space-y-2 mt-1">
					<li class="flex gap-2"><span class="text-accent mt-0.5">▸</span><span><strong>Discount Ads Win:</strong> Across every city, Discount Ads generated higher total profit than Collection Ads.</span></li>
					<li class="flex gap-2"><span class="text-accent mt-0.5">▸</span><span><strong>Profit Leaders:</strong> In Manchester, Discount Ads generated £359K in profit vs. £234K from Collection Ads.</span></li>
				</ul>
			</div>
		</div>

		<!-- 4 -->
		<div class="card bg-base-200 card-md">
			<div class="card-body gap-3">
				<div class="flex items-center gap-3">
					<span class="badge badge-info badge-soft badge-lg">04</span>
					<h3 class="card-title font-display text-lg">The "Engagement Trap"</h3>
				</div>
				<p class="font-sans text-base-content/70 text-sm leading-relaxed">
					A crucial finding: high social engagement (likes, shares, comments) does not always correlate with high conversion rates.
				</p>
				<ul class="font-sans text-sm text-base-content/75 space-y-2 mt-1">
					<li class="flex gap-2"><span class="text-neutral-content/50 mt-0.5">▸</span><span><strong>Misleading Metrics:</strong> Campaigns with high interaction on Facebook often resulted in lower ROI compared to lower-engagement campaigns on Pinterest.</span></li>
				</ul>
			</div>
		</div>

	</div>
</div>
