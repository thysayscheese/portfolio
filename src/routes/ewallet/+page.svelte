<script lang="ts">
	import { resolve } from '$app/paths';

	const findings = [
		{
			number: '01',
			title: 'Version-Specific Regressions',
			description: 'App versions 3.9.5–3.9.9 produced a massive failure surge. A targeted hotfix to these releases alone would recover the majority of lost transactions.',
		},
		{
			number: '02',
			title: '3DS Handshake Gap',
			description: '68.2% of users who reached card confirmation never arrived at the 3DS authentication screen — a silent redirect failure in the backend payment flow.',
		},
		{
			number: '03',
			title: 'Infrastructure Stress',
			description: 'Timeouts (3.0%) and 3DS session expirations (13.9%) both spiked during the 10AM–5PM window, pointing to under-provisioned capacity at peak load.',
		},
		{
			number: '04',
			title: 'Codebase Instability',
			description: 'Web and Tablet platforms shared a 13.3% failure rate, isolating the issue to a core web codebase bug rather than a device-level or network problem.',
		},
		{
			number: '05',
			title: 'Authentication Friction',
			description: '14.1% of users submitted invalid OTPs — a signal of interface friction: small fields, expired timers, and no auto-read SMS capability.',
		},
	];

	const roadmap = [
		{
			phase: 'Phase 1',
			label: 'Immediate Stabilization',
			effort: 'Low Effort / High Impact',
			effortColor: 'badge-success',
			actions: [
				'Adjust payment timeout thresholds to reduce peak-hour expirations',
				'Promote wallet payments as a high-reliability alternative',
				'Deploy real-time monitoring dashboards for transaction funnel visibility',
			],
		},
		{
			phase: 'Phase 2',
			label: 'Engineering Remediation',
			effort: 'Targeted Fixes',
			effortColor: 'badge-warning',
			actions: [
				'Issue hotfixes for app versions 3.9.5–3.9.9',
				'Fix 3DS redirect logic in the backend payment service',
				'Resolve core web codebase bug affecting Web and Tablet',
			],
		},
		{
			phase: 'Phase 3',
			label: 'Long-Term Prevention',
			effort: 'Strategic Investment',
			effortColor: 'badge-info',
			actions: [
				'UX overhaul: auto-read SMS OTP, clearer field design, countdown timers',
				'Expand regression test coverage to catch version-specific failures early',
				'Establish performance benchmarks and automated alerting thresholds',
			],
		},
	];
</script>

<svelte:head>
	<title>App Optimization Analysis · Thy Tran</title>
</svelte:head>

<div class="max-w-6xl mx-auto px-6 sm:px-10 pt-16 pb-24">

	<a href={resolve('/projects')} class="text-sm font-sans text-base-content/40 hover:text-primary transition-colors">
		← Back to Projects
	</a>

	<!-- Header -->
	<div class="mt-10 mb-12">
		<span class="badge badge-primary badge-soft mb-4">Product Analytics</span>
		<h1 class="font-display text-5xl lg:text-6xl font-bold leading-tight mb-3">
			App Optimization Analysis
		</h1>
		<p class="font-sans text-base-content/50 text-lg">E-Wallet Payment Analysis · July 2023</p>
		<div class="w-12 h-px bg-primary mt-8"></div>
	</div>

	<!-- Main grid: background + embed -->
	<div class="grid grid-cols-1 lg:grid-cols-[1fr_1.4fr] gap-10 mb-16 items-start">

		<!-- Background -->
		<div>
			<h2 class="font-display text-2xl font-semibold mb-4">Background</h2>
			<p class="font-sans text-base-content/75 text-base leading-relaxed mb-4">
				In July 2023, E-Wallet platform hit a critical performance bottleneck. Despite a steady volume of approximately 500 daily transaction requests, the overall transaction success rate fell sharply from <strong>92% to 82%</strong> — a 10-point drop that translated directly to revenue loss and user frustration.
			</p>
			<p class="font-sans text-base-content/75 text-base leading-relaxed">
				The project analyzes the decline in bill payment success rate since August 2025 using transactional, session, event log, and error data. Power BI and the MECE framework were applied to identify failure points across the payment journey, including authentication, gateway redirects, and app version issues. Key insights highlighted correlations between failure rates and user segments, device types, and network quality. The analysis led to actionable recommendations to optimize payment flows and reduce error impact.
			</p>
		</div>

		<!-- Canva embed -->
		<div class="relative w-full rounded-2xl overflow-hidden shadow-xl border border-base-300" style="padding-top: 56.25%;">
			<iframe
				loading="lazy"
				src="https://www.canva.com/design/DAG-qa_uyoE/Itdey-OXHmT0YVlXdyj5-w/view?embed"
				class="absolute inset-0 w-full h-full border-0"
				allowfullscreen
				title="E-Wallet App Optimization Analysis"
			></iframe>
		</div>
	</div>

	<div class="w-full h-px bg-base-300 mb-16"></div>

	<!-- Key Findings -->
	<div class="mb-16">
		<h2 class="font-display text-3xl font-bold mb-8">Key Findings</h2>
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5">
			{#each findings as f}
				<div class="card bg-base-200 border border-base-300 p-6">
					<p class="font-sans text-3xl font-bold text-primary/30 mb-3">{f.number}</p>
					<h3 class="font-display text-lg font-semibold mb-2">{f.title}</h3>
					<p class="font-sans text-sm text-base-content/65 leading-relaxed">{f.description}</p>
				</div>
			{/each}
		</div>
	</div>

	<div class="w-full h-px bg-base-300 mb-16"></div>

	<!-- Roadmap -->
	<div>
		<h2 class="font-display text-3xl font-bold mb-8">Remediation Roadmap</h2>
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			{#each roadmap as r}
				<div class="card bg-base-200 border border-base-300 p-6 flex flex-col gap-4">
					<div>
						<p class="font-sans text-xs text-base-content/40 uppercase tracking-widest mb-1">{r.phase}</p>
						<h3 class="font-display text-xl font-bold mb-2">{r.label}</h3>
						<span class="badge badge-soft {r.effortColor} text-xs">{r.effort}</span>
					</div>
					<ul class="font-sans text-sm text-base-content/70 leading-relaxed flex flex-col gap-2">
						{#each r.actions as action}
							<li class="flex gap-2">
								<span class="text-primary mt-0.5">›</span>
								<span>{action}</span>
							</li>
						{/each}
					</ul>
				</div>
			{/each}
		</div>
	</div>

</div>
