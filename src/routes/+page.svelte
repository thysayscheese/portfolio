<script>
import { resolve } from '$app/paths';
</script>

<svelte:head>
<title>Thy Tran Portfolio</title>
</svelte:head>

<!-- Navbar -->
<div class="navbar bg-base-100 shadow-sm sticky top-0 z-50">
<div class="navbar-start">
<a href="/" class="btn btn-ghost text-xl font-bold">Thy Tran</a>
</div>
<div class="navbar-center hidden lg:flex">
<ul class="menu menu-horizontal px-1">
<li><a href="#about">About</a></li>
<li><a href="#skills">Skills</a></li>
<li><a href="#work">Work</a></li>
<li><a href="#contact">Contact</a></li>
</ul>
</div>
<div class="navbar-end">
<a href={resolve('/marketing-dashboard')} class="btn btn-primary btn-sm">View Dashboard →</a>
</div>
</div>

<!-- Hero -->
<section class="hero min-h-[calc(100vh-4rem)] bg-base-200" id="about">
<div class="hero-content text-center">
<div class="max-w-2xl">
<div class="avatar avatar-placeholder mb-6">
<div class="bg-primary text-primary-content w-24 rounded-full">
<span class="text-3xl font-bold">TT</span>
</div>
</div>
<h1 class="text-6xl font-bold">Thy Tran</h1>
<p class="py-6 text-xl text-base-content/70">
Turning data challenges into growth and support.
</p>
<div class="flex flex-wrap gap-3 justify-center mb-8">
<span class="badge badge-primary badge-lg">Marketing</span>
<span class="badge badge-secondary badge-lg">Data Analytics</span>
<span class="badge badge-accent badge-lg">Strategy</span>
</div>
<div class="flex flex-wrap gap-3 justify-center">
<a href="#work" class="btn btn-primary">See My Work</a>
<a href="#contact" class="btn btn-outline">Get in Touch</a>
</div>
</div>
</div>
</section>

<!-- Stats -->
<section class="py-16 bg-base-100" id="skills">
<div class="max-w-5xl mx-auto px-6">
<h2 class="text-3xl font-bold text-center mb-12">By the Numbers</h2>
<div class="stats stats-vertical sm:stats-horizontal shadow w-full">
<div class="stat">
<div class="stat-title">Projects Completed</div>
<div class="stat-value text-primary">12+</div>
<div class="stat-desc">Across marketing and analytics</div>
</div>
<div class="stat">
<div class="stat-title">Years of Experience</div>
<div class="stat-value text-secondary">3+</div>
<div class="stat-desc">In digital marketing</div>
</div>
<div class="stat">
<div class="stat-title">Dashboards Built</div>
<div class="stat-value text-accent">5+</div>
<div class="stat-desc">Data-driven insights</div>
</div>
</div>
</div>
</section>

<!-- Skills Cards -->
<section class="py-16 bg-base-200">
<div class="max-w-5xl mx-auto px-6">
<h2 class="text-3xl font-bold text-center mb-12">What I Do</h2>
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
<div class="card bg-base-100 card-md shadow">
<div class="card-body">
<h3 class="card-title">📊 Data Analytics</h3>
<p>Turning raw numbers into actionable insights with dashboards and reports that drive decisions.</p>
<div class="card-actions mt-4 flex-wrap gap-2">
<span class="badge badge-soft badge-primary">SQL</span>
<span class="badge badge-soft badge-primary">Tableau</span>
<span class="badge badge-soft badge-primary">Excel</span>
</div>
</div>
</div>
<div class="card bg-base-100 card-md shadow">
<div class="card-body">
<h3 class="card-title">📣 Digital Marketing</h3>
<p>Crafting campaigns and strategies that connect brands to audiences and grow engagement.</p>
<div class="card-actions mt-4 flex-wrap gap-2">
<span class="badge badge-soft badge-secondary">SEO</span>
<span class="badge badge-soft badge-secondary">SEM</span>
<span class="badge badge-soft badge-secondary">Social</span>
</div>
</div>
</div>
<div class="card bg-base-100 card-md shadow">
<div class="card-body">
<h3 class="card-title">🎯 Strategy</h3>
<p>Building go-to-market plans and growth strategies grounded in data and market research.</p>
<div class="card-actions mt-4 flex-wrap gap-2">
<span class="badge badge-soft badge-accent">Research</span>
<span class="badge badge-soft badge-accent">Planning</span>
<span class="badge badge-soft badge-accent">KPIs</span>
</div>
</div>
</div>
</div>
</div>
</section>

<!-- Work / Projects -->
<section class="py-16 bg-base-100" id="work">
<div class="max-w-5xl mx-auto px-6">
<h2 class="text-3xl font-bold text-center mb-12">Featured Work</h2>
<div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
<div class="card bg-base-200 card-md shadow-md hover:shadow-lg transition-shadow">
<div class="card-body">
<div class="flex items-center gap-3 mb-2">
<span class="text-2xl">📈</span>
<h3 class="card-title">Marketing Dashboard</h3>
</div>
<p class="text-base-content/70">
An interactive analytics dashboard visualizing marketing performance, channel attribution, and campaign ROI.
</p>
<div class="card-actions justify-between items-center mt-4">
<div class="flex gap-2 flex-wrap">
<span class="badge badge-soft badge-primary">SvelteKit</span>
<span class="badge badge-soft badge-primary">Charts</span>
</div>
<a href={resolve('/marketing-dashboard')} class="btn btn-primary btn-sm">View →</a>
</div>
</div>
</div>
<div class="card bg-base-200 card-md shadow-md">
<div class="card-body">
<div class="flex items-center gap-3 mb-2">
<span class="text-2xl">🚀</span>
<h3 class="card-title">More Coming Soon</h3>
</div>
<p class="text-base-content/70">
New projects are in the works — check back soon for case studies, brand campaigns, and data deep-dives.
</p>
<div class="card-actions mt-4">
<span class="badge badge-ghost">In Progress</span>
</div>
</div>
</div>
</div>
</div>
</section>

<!-- Contact CTA -->
<section class="py-20 bg-primary text-primary-content" id="contact">
<div class="max-w-2xl mx-auto px-6 text-center">
<h2 class="text-4xl font-bold mb-4">Let's Connect</h2>
<p class="text-primary-content/80 text-lg mb-8">
Always open to new opportunities, collaborations, and conversations.
</p>
<div class="flex flex-wrap gap-4 justify-center">
<a href="mailto:thy@example.com" class="btn btn-outline btn-lg" style="color: oklch(var(--pc)); border-color: oklch(var(--pc));">
✉ Email Me
</a>
<a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" class="btn btn-outline btn-lg" style="color: oklch(var(--pc)); border-color: oklch(var(--pc));">
LinkedIn
</a>
</div>
</div>
</section>

<!-- Footer -->
<footer class="footer footer-center bg-base-300 text-base-content p-10">
<nav class="grid grid-flow-col gap-6">
<a href="#about" class="link link-hover">About</a>
<a href="#skills" class="link link-hover">Skills</a>
<a href="#work" class="link link-hover">Work</a>
<a href="#contact" class="link link-hover">Contact</a>
<a href={resolve('/marketing-dashboard')} class="link link-hover">Dashboard</a>
</nav>
<aside>
<p>© 2026 Thy Tran · Built with SvelteKit & daisyUI</p>
</aside>
</footer>
