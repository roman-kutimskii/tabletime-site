<script lang="ts">
	import { resolve } from '$app/paths';
</script>

<svelte:head>
	<title>Услуги - TableTime</title>
	<meta
		name="description"
		content="Услуги TableTime для ресторанов: онлайн-бронирование, управление столиками, аналитика и продвижение. Узнайте о наших тарифах и возможностях."
	/>
</svelte:head>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h1>Наши услуги</h1>
			<p class="text-muted">
				Комплексные решения для управления бронированиями в вашем ресторане
			</p>
		</div>

		<div class="grid grid-2">
			<div class="card service-card">
				<div class="service-icon">📅</div>
				<h2>Онлайн-бронирование</h2>
				<p>
					Предоставьте вашим клиентам возможность легко бронировать столики онлайн через
					веб-сайт или мобильное приложение. Интеграция с вашим сайтом и социальными сетями.
				</p>
				<ul class="service-features">
					<li>Круглосуточное бронирование</li>
					<li>Автоматическое подтверждение</li>
					<li>Напоминания клиентам</li>
					<li>Интеграция с календарем</li>
				</ul>
			</div>

			<div class="card service-card">
				<div class="service-icon">🖥️</div>
				<h2>Панель управления</h2>
				<p>
					Удобная панель управления для контроля всех бронирований в режиме реального времени.
					Управляйте столиками, временными слотами и доступностью.
				</p>
				<ul class="service-features">
					<li>Управление столиками</li>
					<li>Календарь бронирований</li>
					<li>История клиентов</li>
					<li>Настройка доступности</li>
				</ul>
			</div>

			<div class="card service-card">
				<div class="service-icon">📊</div>
				<h2>Аналитика и отчеты</h2>
				<p>
					Получайте детальную аналитику по бронированиям, популярным временам, дням недели и
					сезонности. Используйте данные для оптимизации работы ресторана.
				</p>
				<ul class="service-features">
					<li>Статистика бронирований</li>
					<li>Анализ загрузки</li>
					<li>Отчеты по периодам</li>
					<li>Экспорт данных</li>
				</ul>
			</div>

			<div class="card service-card">
				<div class="service-icon">📱</div>
				<h2>Мобильное приложение</h2>
				<p>
					Мобильное приложение для ваших клиентов позволяет им легко находить и бронировать
					столики прямо со смартфона.
				</p>
				<ul class="service-features">
					<li>Поиск ресторанов</li>
					<li>Быстрое бронирование</li>
					<li>Уведомления</li>
					<li>История бронирований</li>
				</ul>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="section-title">
			<h2>Преимущества платформы</h2>
		</div>
		<div class="grid grid-3">
			<div class="benefit-item">
				<h3>⚡ Быстрая интеграция</h3>
				<p>Подключение займет всего несколько минут. Наша команда поможет с настройкой.</p>
			</div>
			<div class="benefit-item">
				<h3>💰 Экономия времени</h3>
				<p>Автоматизация процесса бронирования освобождает время вашего персонала.</p>
			</div>
			<div class="benefit-item">
				<h3>📈 Увеличение загрузки</h3>
				<p>Улучшите заполняемость ресторана за счет удобного онлайн-бронирования.</p>
			</div>
			<div class="benefit-item">
				<h3>👥 Улучшение сервиса</h3>
				<p>Предоставьте клиентам современный и удобный способ бронирования столиков.</p>
			</div>
			<div class="benefit-item">
				<h3>🔒 Безопасность данных</h3>
				<p>Все данные защищены современными методами шифрования и соответствуют стандартам.</p>
			</div>
			<div class="benefit-item">
				<h3>🛠️ Техподдержка</h3>
				<p>Наша команда поддержки всегда готова помочь с любыми вопросами.</p>
			</div>
		</div>
	</div>
</section>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h2>Тарифные планы</h2>
			<p class="text-muted">Выберите план, который подходит вашему ресторану</p>
		</div>
		<div class="grid grid-3">
			<div class="card pricing-card">
				<h3>Базовый</h3>
				<div class="price">
					<span class="price-amount">5 000 ₽</span>
					<span class="price-period">/месяц</span>
				</div>
				<ul class="pricing-features">
					<li>До 50 бронирований/месяц</li>
					<li>Базовая панель управления</li>
					<li>Email поддержка</li>
					<li>Базовые отчеты</li>
				</ul>
				<a href={resolve('/contacts')} class="btn btn-outline">Связаться</a>
			</div>

			<div class="card pricing-card featured">
				<div class="badge">Популярный</div>
				<h3>Стандартный</h3>
				<div class="price">
					<span class="price-amount">10 000 ₽</span>
					<span class="price-period">/месяц</span>
				</div>
				<ul class="pricing-features">
					<li>До 200 бронирований/месяц</li>
					<li>Расширенная панель управления</li>
					<li>Приоритетная поддержка</li>
					<li>Детальная аналитика</li>
					<li>Интеграция с сайтом</li>
				</ul>
				<a href={resolve('/contacts')} class="btn btn-primary">Связаться</a>
			</div>

			<div class="card pricing-card">
				<h3>Премиум</h3>
				<div class="price">
					<span class="price-amount">20 000 ₽</span>
					<span class="price-period">/месяц</span>
				</div>
				<ul class="pricing-features">
					<li>Неограниченные бронирования</li>
					<li>Все функции платформы</li>
					<li>Персональный менеджер</li>
					<li>Расширенная аналитика</li>
					<li>API интеграция</li>
					<li>Кастомные решения</li>
				</ul>
				<a href={resolve('/contacts')} class="btn btn-outline">Связаться</a>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="cta-section">
			<h2>Готовы начать?</h2>
			<p>Заполните форму заявки, и мы свяжемся с вами для обсуждения условий подключения.</p>
			<a href={resolve('/contacts')} class="btn btn-primary btn-large">Подать заявку</a>
		</div>
	</div>
</section>

<style>
	.service-card {
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.service-icon {
		font-size: 3rem;
		margin-bottom: var(--spacing-md);
		text-align: center;
	}

	.service-features {
		list-style: none;
		margin-top: var(--spacing-md);
		padding: 0;
	}

	.service-features li {
		padding: var(--spacing-xs) 0;
		padding-left: var(--spacing-lg);
		position: relative;
	}

	.service-features li::before {
		content: '✓';
		position: absolute;
		left: 0;
		color: var(--color-secondary);
		font-weight: bold;
	}

	.benefit-item {
		text-align: center;
		padding: var(--spacing-lg);
	}

	.benefit-item h3 {
		margin-bottom: var(--spacing-sm);
	}

	.pricing-card {
		text-align: center;
		position: relative;
		display: flex;
		flex-direction: column;
		height: 100%;
	}

	.pricing-card.featured {
		border: 2px solid var(--color-primary);
		transform: scale(1.05);
	}

	.badge {
		position: absolute;
		top: -12px;
		left: 50%;
		transform: translateX(-50%);
		background-color: var(--color-accent);
		color: var(--color-white);
		padding: var(--spacing-xs) var(--spacing-md);
		border-radius: var(--border-radius);
		font-size: var(--font-size-sm);
		font-weight: var(--font-weight-semibold);
	}

	.price {
		margin: var(--spacing-lg) 0;
	}

	.price-amount {
		font-size: var(--font-size-3xl);
		font-weight: var(--font-weight-bold);
		color: var(--color-primary);
	}

	.price-period {
		color: var(--color-text-light);
		font-size: var(--font-size-base);
	}

	.pricing-features {
		list-style: none;
		margin: var(--spacing-lg) 0;
		padding: 0;
		flex-grow: 1;
	}

	.pricing-features li {
		padding: var(--spacing-sm) 0;
		border-bottom: 1px solid var(--color-border);
	}

	.pricing-features li:last-child {
		border-bottom: none;
	}

	.btn-large {
		padding: var(--spacing-md) var(--spacing-xl);
		font-size: var(--font-size-lg);
	}

	.cta-section {
		text-align: center;
		padding: var(--spacing-2xl);
	}

	.cta-section h2 {
		margin-bottom: var(--spacing-md);
	}

	.cta-section p {
		margin-bottom: var(--spacing-xl);
		color: var(--color-text-light);
	}

	@media (max-width: 1024px) {
		.pricing-card.featured {
			transform: scale(1);
		}
	}

	@media (max-width: 768px) {
		.grid-2,
		.grid-3 {
			grid-template-columns: 1fr;
		}
	}
</style>
