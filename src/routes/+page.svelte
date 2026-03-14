<script>
import { resolve } from '$app/paths';
</script>

<svelte:head>
<title>Thy Tran</title>
</svelte:head>

<section class="min-h-screen flex items-center bg-base-100">
<div class="max-w-6xl w-full mx-auto px-8 sm:px-12 py-16 grid grid-cols-1 lg:grid-cols-[1fr_auto] gap-12 lg:gap-20 items-center">

	<!-- Left: text -->
	<div>
		<p class="text-xs font-sans font-medium text-primary uppercase tracking-widest mb-3">
			Portfolio
		</p>

		<h1 class="font-display text-5xl lg:text-6xl font-bold leading-tight mb-3">
			Thy Tran
		</h1>

		<p class="font-sans text-base-content/50 text-xs tracking-wide mb-7">
			Sales Business Analyst &nbsp;·&nbsp; Marketing &nbsp;·&nbsp; Data
		</p>

		<div class="w-10 h-px bg-primary mb-7"></div>

		<p class="font-sans text-base-content/70 text-sm leading-relaxed mb-4">
			Hi, I'm Thy! Originally from Saigon and now based in Germany for nine years, my career has been a journey of turning challenges into growth. With a background in International Management and Marketing (FAU Nürnberg), I've spent years in Sales and Marketing at companies like Ergobaby, Henkel, and Körber AG.
		</p>

		<p class="font-sans text-base-content/70 text-sm leading-relaxed mb-9">
			I'm currently a Sales Business Analyst at Ergobaby. I thrive on transforming complex sales data into clear visualizations, dashboards, and pricing strategies. I embrace every analytical challenge as a path to growth and a means to support the people around me. I'm passionate about using data to create a positive impact for my team and the business.
		</p>

		<a href={resolve('/projects')} class="btn btn-primary btn-sm text-sm font-normal">
			View My Projects →
		</a>
	</div>

	<!-- Right: portrait -->
	<div class="hidden lg:flex justify-center items-center self-center">
		<div class="w-58 h-58 rounded-full overflow-hidden shrink-0 ring-2 ring-base-300 bg-slate-600">
			<img
				src="/portrait.png"
				alt="Thy Tran"
				class="w-full h-full object-cover object-top "
				draggable="false"
			/>
		</div>
	</div>

</div>
</section>
