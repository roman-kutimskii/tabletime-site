<script lang="ts">
	import { page } from '$app/stores';
	import { resolve } from '$app/paths';
	import { onMount } from 'svelte';

	let mobileMenuOpen = $state(false);

	const navItems = [
		{ href: resolve('/'), path: '/', label: 'Главная' },
		{ href: resolve('/about'), path: '/about', label: 'О нас' },
		{ href: resolve('/services'), path: '/services', label: 'Услуги' },
		{ href: resolve('/contacts'), path: '/contacts', label: 'Контакты' }
	];

	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}

	function closeMobileMenu() {
		mobileMenuOpen = false;
	}

	onMount(() => {
		// Закрываем мобильное меню при изменении страницы
		return () => {
			mobileMenuOpen = false;
		};
	});
</script>

<nav class="navbar">
	<div class="nav-container">
		<a href={resolve('/')} class="logo">
			<span class="logo-text">TableTime</span>
		</a>

		<button
			class="mobile-menu-toggle"
			aria-label="Toggle menu"
			aria-expanded={mobileMenuOpen}
			onclick={toggleMobileMenu}
		>
			<span class="hamburger-line"></span>
			<span class="hamburger-line"></span>
			<span class="hamburger-line"></span>
		</button>

		<ul class="nav-menu" class:active={mobileMenuOpen}>
			{#each navItems as item (item.href)}
				<li>
					<a
						href={item.href}
						class:active={$page.url.pathname === item.path || $page.url.pathname === item.href}
						onclick={closeMobileMenu}
					>
						{item.label}
					</a>
				</li>
			{/each}
		</ul>
	</div>
</nav>

<style>
	.navbar {
		background-color: var(--color-primary);
		color: var(--color-white);
		padding: 1rem 0;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
		position: sticky;
		top: 0;
		z-index: 1000;
	}

	.nav-container {
		max-width: var(--container-max-width);
		margin: 0 auto;
		padding: 0 var(--spacing-md);
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.logo {
		font-size: 1.5rem;
		font-weight: bold;
		text-decoration: none;
		color: var(--color-white);
		transition: opacity 0.2s;
	}

	.logo:hover {
		opacity: 0.8;
	}

	.logo-text {
		color: var(--color-white);
	}

	.mobile-menu-toggle {
		display: none;
		flex-direction: column;
		background: none;
		border: none;
		cursor: pointer;
		padding: 0.5rem;
		gap: 4px;
	}

	.hamburger-line {
		width: 25px;
		height: 3px;
		background-color: var(--color-white);
		transition: all 0.3s;
		border-radius: 2px;
	}

	.nav-menu {
		display: flex;
		list-style: none;
		margin: 0;
		padding: 0;
		gap: 2rem;
		align-items: center;
	}

	.nav-menu li {
		margin: 0;
	}

	.nav-menu a {
		color: var(--color-white);
		text-decoration: none;
		font-weight: 500;
		padding: 0.5rem 1rem;
		border-radius: 4px;
		transition: background-color 0.2s;
		display: block;
	}

	.nav-menu a:hover {
		background-color: rgba(255, 255, 255, 0.1);
	}

	.nav-menu a.active {
		background-color: rgba(255, 255, 255, 0.2);
	}

	@media (max-width: 768px) {
		.mobile-menu-toggle {
			display: flex;
		}

		.nav-menu {
			position: fixed;
			top: 60px;
			left: 0;
			right: 0;
			background-color: var(--color-primary);
			flex-direction: column;
			padding: 2rem 0;
			gap: 0;
			transform: translateX(-100%);
			transition: transform 0.3s ease-in-out;
			box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
		}

		.nav-menu.active {
			transform: translateX(0);
		}

		.nav-menu li {
			width: 100%;
		}

		.nav-menu a {
			padding: 1rem 2rem;
			width: 100%;
			text-align: left;
		}

		.mobile-menu-toggle[aria-expanded='true'] .hamburger-line:nth-child(1) {
			transform: rotate(45deg) translate(5px, 5px);
		}

		.mobile-menu-toggle[aria-expanded='true'] .hamburger-line:nth-child(2) {
			opacity: 0;
		}

		.mobile-menu-toggle[aria-expanded='true'] .hamburger-line:nth-child(3) {
			transform: rotate(-45deg) translate(5px, -5px);
		}
	}
</style>
