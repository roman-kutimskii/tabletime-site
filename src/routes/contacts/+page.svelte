<script lang="ts">
	import RestaurantForm from '$lib/components/RestaurantForm.svelte';
</script>

<svelte:head>
	<title>Контакты - TableTime</title>
	<meta
		name="description"
		content="Свяжитесь с нами - TableTime. Адрес, телефон, email. Заполните форму заявки для подключения вашего ресторана."
	/>
</svelte:head>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h1>Контакты</h1>
			<p class="text-muted">Свяжитесь с нами любым удобным способом</p>
		</div>

		<div class="contacts-grid">
			<div class="contacts-info">
				<div class="card contact-card">
					<div class="contact-icon">📍</div>
					<h3>Адрес</h3>
					<p>г. Москва, ул. Примерная, д. 1</p>
					<p class="text-muted">Бизнес-центр "Пример", офис 101</p>
				</div>

				<div class="card contact-card">
					<div class="contact-icon">📞</div>
					<h3>Телефон</h3>
					<p>
						<a href="tel:+79991234567">+7 (999) 123-45-67</a>
					</p>
					<p class="text-muted">Пн-Пт: 9:00 - 18:00</p>
				</div>

				<div class="card contact-card">
					<div class="contact-icon">✉️</div>
					<h3>Email</h3>
					<p>
						<a href="mailto:info@tabletime.ru">info@tabletime.ru</a>
					</p>
					<p class="text-muted">Ответим в течение 24 часов</p>
				</div>

				<div class="card contact-card">
					<div class="contact-icon">💬</div>
					<h3>Социальные сети</h3>
					<div class="social-links">
						<a href="#" class="social-link">Telegram</a>
						<a href="#" class="social-link">WhatsApp</a>
						<a href="#" class="social-link">VK</a>
					</div>
				</div>
			</div>

			<div class="map-container">
				<div class="card">
					<h3>Как нас найти</h3>
					<div class="map-placeholder">
						<span>Карта (заглушка)</span>
						<p class="text-muted">Здесь будет интерактивная карта</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="section-title">
			<h2>Подать заявку на подключение</h2>
			<p class="text-muted">
				Заполните форму ниже, и мы свяжемся с вами для обсуждения условий подключения вашего
				ресторана к платформе TableTime.
			</p>
		</div>
		<RestaurantForm />
	</div>
</section>

<style>
	.contacts-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: var(--spacing-xl);
		margin-bottom: var(--spacing-3xl);
	}

	.contacts-info {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: var(--spacing-lg);
	}

	.contact-card {
		text-align: center;
		padding: var(--spacing-lg);
	}

	.contact-icon {
		font-size: 2.5rem;
		margin-bottom: var(--spacing-md);
	}

	.contact-card h3 {
		margin-bottom: var(--spacing-sm);
	}

	.contact-card p {
		margin-bottom: var(--spacing-xs);
	}

	.contact-card a {
		color: var(--color-primary);
		font-weight: var(--font-weight-medium);
	}

	.contact-card a:hover {
		text-decoration: underline;
	}

	.social-links {
		display: flex;
		gap: var(--spacing-md);
		justify-content: center;
		flex-wrap: wrap;
		margin-top: var(--spacing-sm);
	}

	.social-link {
		padding: var(--spacing-xs) var(--spacing-md);
		background-color: var(--color-primary);
		color: var(--color-white);
		border-radius: var(--border-radius);
		transition: background-color var(--transition-base);
	}

	.social-link:hover {
		background-color: var(--color-primary-dark);
		color: var(--color-white);
	}

	.map-container {
		width: 100%;
	}

	.map-placeholder {
		background-color: var(--color-border);
		border-radius: var(--border-radius);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		color: var(--color-text-light);
		min-height: 400px;
		font-size: var(--font-size-lg);
		padding: var(--spacing-xl);
	}

	.map-placeholder span {
		margin-bottom: var(--spacing-md);
	}

	@media (max-width: 1024px) {
		.contacts-grid {
			grid-template-columns: 1fr;
		}

		.contacts-info {
			grid-template-columns: 1fr;
		}
	}

	@media (max-width: 768px) {
		.contacts-info {
			grid-template-columns: 1fr;
		}

		.map-placeholder {
			min-height: 300px;
		}
	}
</style>
