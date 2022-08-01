<script context="module" lang="ts">
	export const prerender = true
	import logo from "$lib/assets/logo.svg"
</script>

<svelte:head>
	<meta name="description" content="Lord Rhubarb's Moose on the Loose Wildlife Tours" />
	<title>Lord Rhubarb's Moose on the Loose Wildlife Tours</title>
	<meta name="title" content="Lord Rhubarb's Moose on the Loose Wildlife Tours" />
	<meta name="description" content="The greatest wildlife tour on earth led by the greatest moose in the galaxy." />

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://wildlife-tours.vercel.app" />
	<meta property="og:title" content="Lord Rhubarb's Moose on the Loose Wildlife Tours" />
	<meta property="og:description" content="The greatest wildlife tour on earth led by the greatest moose in the galaxy." />
	<meta
		property="og:image"
		content="https://images.unsplash.com/photo-1602391950852-88bf9be72b24?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1600&q=80" />

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://wildlife-tours.vercel.app" />
	<meta property="twitter:title" content="Lord Rhubarb's Moose on the Loose Wildlife Tours" />
	<meta property="twitter:description" content="The greatest wildlife tour on earth led by the greatest moose in the galaxy." />
	<meta
		property="twitter:image"
		content="https://images.unsplash.com/photo-1602391950852-88bf9be72b24?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1600&q=80" />
</svelte:head>

<main>
	<div class="content">
		<h1>Lord Rhubarb's Moose on the Loose Wildlife Tours</h1>
		<img class="logo" src={logo} alt="logo" />
	</div>
	<div class="img-container">
		<div class="overlay" />
		<img
			src="https://images.unsplash.com/photo-1602391950852-88bf9be72b24?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1600&q=80"
			alt="" />
	</div>
</main>

<style lang="scss">
	main {
		position: relative;
		height: 100vh;
		margin: 0;
		overflow: hidden;
	}
	.content {
		position: absolute;
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		height: 100%;
		padding: 50px;
	}
	.logo {
		height: 50%;
		max-width: 80%;
	}

	h1 {
		display: none;
	}

	.img-container {
		height: 100%;
		width: 100%;
		z-index: -1;
		position: relative;
		& .overlay {
			background-color: black;
			opacity: 0.3;
			height: 100%;
			width: 100%;
			position: absolute;
		}
		& img {
			height: 100%;
			width: 100%;
			object-fit: cover;
		}
	}
</style>
