<script>
	import { resolve } from '$app/paths';
</script>

<svelte:head>
	<title>Thy Tran Portfolio</title>
</svelte:head>

<main class="min-h-screen flex items-center justify-center">
	<div class="text-center">
		<h1 class="text-4xl font-bold mb-8">Thy Tran</h1>
		<a
			href={resolve('/marketing-dashboard')}
			class="inline-block px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors text-lg"
		>
			Marketing Dashboard
		</a>
	</div>
</main>
