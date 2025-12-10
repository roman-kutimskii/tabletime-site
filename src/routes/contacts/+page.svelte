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
					<p>г. Йошкар-Ола, ул. Петрова, д. 12А</p>
					<p class="text-muted">Корпус 2, офис 5</p>
				</div>

				<div class="card contact-card">
					<div class="contact-icon">📞</div>
					<h3>Телефон</h3>
					<p>
						<a href="tel:+793712345657">+7 (937) 123-45-67</a>
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
						<a
							href="https://t.me"
							target="_blank"
							rel="noopener noreferrer"
							class="social-link">Telegram</a
						>
						<a
							href="https://wa.me"
							target="_blank"
							rel="noopener noreferrer"
							class="social-link">WhatsApp</a
						>
						<a
							href="https://vk.com"
							target="_blank"
							rel="noopener noreferrer"
							class="social-link">VK</a
						>
					</div>
				</div>
			</div>

			<div class="map-container">
				<div class="card">
					<h3>Как нас найти</h3>
					<div class="map-placeholder">
						<div style="position:relative;overflow:hidden;display: flex; flex-direction: column; flex: 1 1 auto;">
							<a
								href="https://yandex.ru/maps/41/yoshkar-ola/?utm_medium=mapframe&utm_source=maps"
								style="color:#eee;font-size:12px;position:absolute;top:0px;">Йошкар‑Ола</a
							><a
								href="https://yandex.ru/maps/41/yoshkar-ola/house/ulitsa_petrova_12a/YE4YfwVjTkYAQFtsfXpycH9gZg==/?ll=47.923632%2C56.630940&utm_medium=mapframe&utm_source=maps&z=17.16"
								style="color:#eee;font-size:12px;position:absolute;top:14px;"
								>Улица Петрова, 12А — Яндекс Карты</a
							><iframe
								src="https://yandex.ru/map-widget/v1/?ll=47.923632%2C56.630940&mode=whatshere&whatshere%5Bpoint%5D=47.923503%2C56.631104&whatshere%5Bzoom%5D=17&z=17.16"
								frameborder="1"
								style="flex: 1 1 auto;"
								title="Карта"
							></iframe>
						</div>
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
		background-color: transparent;
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
		justify-content: center;
		color: var(--color-text-light);
		min-height: 400px;
		font-size: var(--font-size-lg);
		padding: var(--spacing-xs);
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
