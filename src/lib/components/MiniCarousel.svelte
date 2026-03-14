<script lang="ts">
	let { slides }: { slides: { src: string; label: string }[] } = $props();

	let current = $state(0);

	function go(i: number) {
		current = (i + slides.length) % slides.length;
	}
</script>

<div class="relative rounded-xl overflow-hidden shadow-lg border border-base-200 bg-base-200 select-none">
	<div class="overflow-hidden">
		{#each slides as slide, i}
			<div class="{i === current ? 'block' : 'hidden'}">
				<img
					src={slide.src}
					alt={slide.label}
					class="w-full object-cover pointer-events-none"
					draggable="false"
				/>
			</div>
		{/each}
	</div>

	<button
		onclick={() => go(current - 1)}
		class="absolute left-2 top-1/2 -translate-y-1/2 btn btn-circle btn-xs bg-base-100/80 border-0 shadow"
		aria-label="Previous"
	>‹</button>
	<button
		onclick={() => go(current + 1)}
		class="absolute right-2 top-1/2 -translate-y-1/2 btn btn-circle btn-xs bg-base-100/80 border-0 shadow"
		aria-label="Next"
	>›</button>

	<span class="absolute bottom-2 left-1/2 -translate-x-1/2 badge badge-neutral badge-xs opacity-75">
		{slides[current].label}
	</span>
</div>

<div class="flex justify-center gap-2 mt-3">
	{#each slides as _, i}
		<button
			onclick={() => go(i)}
			class="w-2 h-2 rounded-full transition-colors {i === current ? 'bg-primary' : 'bg-base-300'}"
			aria-label="Go to slide {i + 1}"
		></button>
	{/each}
</div>
