<script lang="ts">
	import RestaurantForm from '$lib/components/RestaurantForm.svelte';
</script>

<svelte:head>
	<title>TableTime - Онлайн-бронирование столиков в ресторанах</title>
	<meta
		name="description"
		content="TableTime - современный сервис для онлайн-бронирования столиков в ресторанах. Удобное управление бронированиями для ресторанов и быстрое бронирование для клиентов."
	/>
</svelte:head>

<section class="hero">
	<div class="container">
		<h1 class="hero-title">TableTime</h1>
		<p class="hero-subtitle">
			Современный сервис для онлайн-бронирования столиков в ресторанах
		</p>
		<div class="hero-actions">
			<a href="/services" class="btn btn-primary">Узнать больше</a>
			<a href="/contacts" class="btn btn-outline">Связаться с нами</a>
		</div>
	</div>
</section>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h2>Почему выбирают TableTime?</h2>
		</div>
		<div class="grid grid-3">
			<div class="card">
				<div class="card-icon">📱</div>
				<h3>Удобное бронирование</h3>
				<p>
					Клиенты могут легко найти свободные столики и забронировать их в несколько кликов
					через веб-сайт или мобильное приложение.
				</p>
			</div>
			<div class="card">
				<div class="card-icon">⚡</div>
				<h3>Управление в реальном времени</h3>
				<p>
					Рестораны получают удобную панель управления для контроля бронирований, аналитики и
					продвижения.
				</p>
			</div>
			<div class="card">
				<div class="card-icon">📊</div>
				<h3>Аналитика и отчеты</h3>
				<p>
					Получайте детальную аналитику по бронированиям, популярным временам и дням недели для
					оптимизации работы ресторана.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="content-grid">
			<div class="content-text">
				<h2>Как это работает?</h2>
				<p>
					TableTime — это веб-сервис для онлайн-бронирования столиков в ресторанах, который
					позволяет пользователям быстро находить свободные места, оформлять бронь и получать
					подтверждение в реальном времени.
				</p>
				<p>
					Сервис предоставляет ресторанам удобную панель управления бронированиями, аналитику и
					инструменты продвижения.
				</p>
				<a href="/about" class="btn btn-primary">Подробнее о нас</a>
			</div>
			<div class="content-media">
				<div class="media-placeholder">
					<span>Видео или изображение</span>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h2>Подключите ваш ресторан</h2>
			<p class="text-muted">
				Заполните форму ниже, и мы свяжемся с вами для обсуждения условий подключения
			</p>
		</div>
		<RestaurantForm />
	</div>
</section>

<style>
	.hero-actions {
		display: flex;
		gap: var(--spacing-md);
		justify-content: center;
		flex-wrap: wrap;
		margin-top: var(--spacing-xl);
	}

	.card-icon {
		font-size: 3rem;
		margin-bottom: var(--spacing-md);
		text-align: center;
	}

	.section-alt {
		background-color: var(--color-bg-light);
	}

	.content-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: var(--spacing-2xl);
		align-items: center;
	}

	.content-text h2 {
		margin-bottom: var(--spacing-lg);
	}

	.content-text p {
		margin-bottom: var(--spacing-md);
	}

	.content-media {
		width: 100%;
	}

	.media-placeholder {
		background-color: var(--color-border);
		border-radius: var(--border-radius-lg);
		display: flex;
		align-items: center;
		justify-content: center;
		color: var(--color-text-light);
		min-height: 300px;
		font-size: var(--font-size-lg);
	}

	@media (max-width: 768px) {
		.content-grid {
			grid-template-columns: 1fr;
		}

		.hero-actions {
			flex-direction: column;
		}

		.hero-actions .btn {
			width: 100%;
		}
	}
</style>