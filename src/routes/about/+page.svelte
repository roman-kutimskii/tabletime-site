<script lang="ts"></script>

<svelte:head>
	<title>О нас - TableTime</title>
	<meta
		name="description"
		content="Узнайте больше о компании TableTime - наша миссия, ценности и команда. Мы создаем современные решения для ресторанного бизнеса."
	/>
</svelte:head>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h1>О компании TableTime</h1>
		</div>

		<div class="content-section">
			<div class="content-text">
				<h2>Наша история</h2>
				<p>
					TableTime был основан с целью упростить процесс бронирования столиков в ресторанах и
					сделать его максимально удобным как для клиентов, так и для владельцев ресторанов.
				</p>
				<p>
					Мы понимаем, что современный ресторанный бизнес требует эффективных инструментов для
					управления бронированиями, и именно поэтому создали платформу, которая объединяет
					удобство для клиентов и мощные инструменты управления для ресторанов.
				</p>
			</div>
			<div class="content-media">
				<div class="media-placeholder">
					<span>Изображение офиса или команды</span>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="section-title">
			<h2>Наша миссия</h2>
		</div>
		<div class="mission-content">
			<p class="mission-text">
				Мы стремимся сделать процесс бронирования столиков максимально простым и удобным,
				предоставляя ресторанам современные инструменты для управления и развития бизнеса, а
				клиентам — быстрый и надежный способ забронировать столик в любимом ресторане.
			</p>
		</div>
	</div>
</section>

<section class="section">
	<div class="container">
		<div class="section-title">
			<h2>Наши ценности</h2>
		</div>
		<div class="grid grid-4">
			<div class="card">
				<h3>Инновации</h3>
				<p>Мы постоянно развиваемся и внедряем новые технологии для улучшения сервиса.</p>
			</div>
			<div class="card">
				<h3>Надежность</h3>
				<p>Мы гарантируем стабильную работу платформы и защиту данных наших клиентов.</p>
			</div>
			<div class="card">
				<h3>Удобство</h3>
				<p>Мы создаем интуитивно понятные интерфейсы для всех пользователей платформы.</p>
			</div>
			<div class="card">
				<h3>Поддержка</h3>
				<p>Мы всегда готовы помочь и ответить на любые вопросы наших партнеров.</p>
			</div>
		</div>
	</div>
</section>

<section class="section section-alt">
	<div class="container">
		<div class="section-title">
			<h2>Наша команда</h2>
		</div>
		<div class="grid grid-3">
			<div class="team-card">
				<div class="team-avatar">
					<div class="media-placeholder" style="min-height: 150px; border-radius: 50%">
						<span>👤</span>
					</div>
				</div>
				<h3>Иван Иванов</h3>
				<p class="team-role">Генеральный директор</p>
				<p class="text-muted">Основатель компании с 10-летним опытом в ресторанном бизнесе</p>
			</div>
			<div class="team-card">
				<div class="team-avatar">
					<div class="media-placeholder" style="min-height: 150px; border-radius: 50%">
						<span>👤</span>
					</div>
				</div>
				<h3>Мария Петрова</h3>
				<p class="team-role">Технический директор</p>
				<p class="text-muted">Эксперт в области разработки веб-приложений и мобильных решений</p>
			</div>
			<div class="team-card">
				<div class="team-avatar">
					<div class="media-placeholder" style="min-height: 150px; border-radius: 50%">
						<span>👤</span>
					</div>
				</div>
				<h3>Алексей Сидоров</h3>
				<p class="team-role">Директор по развитию</p>
				<p class="text-muted">Специалист по работе с партнерами и развитию бизнеса</p>
			</div>
		</div>
	</div>
</section>

<style>
	.content-section {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: var(--spacing-2xl);
		align-items: center;
		margin-bottom: var(--spacing-3xl);
	}

	.content-text h2 {
		margin-bottom: var(--spacing-lg);
	}

	.content-text p {
		margin-bottom: var(--spacing-md);
	}

	.mission-content {
		max-width: 800px;
		margin: 0 auto;
		text-align: center;
	}

	.mission-text {
		font-size: var(--font-size-lg);
		line-height: 1.8;
		color: var(--color-text-light);
	}

	.team-card {
		text-align: center;
		padding: var(--spacing-lg);
	}

	.team-avatar {
		margin-bottom: var(--spacing-md);
		display: flex;
		justify-content: center;
	}

	.team-role {
		font-weight: var(--font-weight-semibold);
		color: var(--color-primary);
		margin-bottom: var(--spacing-sm);
	}

	@media (max-width: 768px) {
		.content-section {
			grid-template-columns: 1fr;
		}

		.mission-text {
			font-size: var(--font-size-base);
		}
	}
</style>
