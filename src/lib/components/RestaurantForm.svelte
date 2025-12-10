<script lang="ts">
	let restaurantName = $state('');
	let contactPerson = $state('');
	let phone = $state('');
	let email = $state('');
	let address = $state('');
	let comment = $state('');
	let submitted = $state(false);
	let errors = $state<Record<string, string>>({});

	function validateEmail(email: string): boolean {
		const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
		return re.test(email);
	}

	function validatePhone(phone: string): boolean {
		const re = /^[\d\s\-\+\(\)]+$/;
		return re.test(phone) && phone.replace(/\D/g, '').length >= 10;
	}

	function validateForm(): boolean {
		errors = {};

		if (!restaurantName.trim()) {
			errors.restaurantName = 'Пожалуйста, введите название ресторана';
		}

		if (!contactPerson.trim()) {
			errors.contactPerson = 'Пожалуйста, введите контактное лицо';
		}

		if (!phone.trim()) {
			errors.phone = 'Пожалуйста, введите телефон';
		} else if (!validatePhone(phone)) {
			errors.phone = 'Пожалуйста, введите корректный номер телефона';
		}

		if (!email.trim()) {
			errors.email = 'Пожалуйста, введите email';
		} else if (!validateEmail(email)) {
			errors.email = 'Пожалуйста, введите корректный email адрес';
		}

		if (!address.trim()) {
			errors.address = 'Пожалуйста, введите адрес ресторана';
		}

		return Object.keys(errors).length === 0;
	}

	function handleSubmit(event: Event) {
		event.preventDefault();

		if (validateForm()) {
			// Frontend-only: просто показываем сообщение об успехе
			submitted = true;

			// Сброс формы через 5 секунд
			setTimeout(() => {
				restaurantName = '';
				contactPerson = '';
				phone = '';
				email = '';
				address = '';
				comment = '';
				submitted = false;
			}, 5000);
		}
	}
</script>

<div class="form-container">
	<h2>Подать заявку на подключение</h2>
	<p class="form-description">
		Заполните форму ниже, и мы свяжемся с вами в ближайшее время для обсуждения условий
		подключения.
	</p>

	{#if submitted}
		<div class="form-success">
			<h3>Спасибо за вашу заявку!</h3>
			<p>Мы получили вашу заявку и свяжемся с вами в ближайшее время.</p>
		</div>
	{:else}
		<form onsubmit={handleSubmit} class="restaurant-form">
			<div class="form-group">
				<label for="restaurantName" class="form-label">
					Название ресторана <span class="required">*</span>
				</label>
				<input
					type="text"
					id="restaurantName"
					bind:value={restaurantName}
					class="form-input"
					class:error={errors.restaurantName}
					placeholder="Введите название ресторана"
				/>
				{#if errors.restaurantName}
					<span class="form-error">{errors.restaurantName}</span>
				{/if}
			</div>

			<div class="form-group">
				<label for="contactPerson" class="form-label">
					Контактное лицо <span class="required">*</span>
				</label>
				<input
					type="text"
					id="contactPerson"
					bind:value={contactPerson}
					class="form-input"
					class:error={errors.contactPerson}
					placeholder="Введите ФИО контактного лица"
				/>
				{#if errors.contactPerson}
					<span class="form-error">{errors.contactPerson}</span>
				{/if}
			</div>

			<div class="form-group">
				<label for="phone" class="form-label">
					Телефон <span class="required">*</span>
				</label>
				<input
					type="tel"
					id="phone"
					bind:value={phone}
					class="form-input"
					class:error={errors.phone}
					placeholder="+7 (999) 123-45-67"
				/>
				{#if errors.phone}
					<span class="form-error">{errors.phone}</span>
				{/if}
			</div>

			<div class="form-group">
				<label for="email" class="form-label">
					Email <span class="required">*</span>
				</label>
				<input
					type="email"
					id="email"
					bind:value={email}
					class="form-input"
					class:error={errors.email}
					placeholder="example@restaurant.ru"
				/>
				{#if errors.email}
					<span class="form-error">{errors.email}</span>
				{/if}
			</div>

			<div class="form-group">
				<label for="address" class="form-label">
					Адрес ресторана <span class="required">*</span>
				</label>
				<input
					type="text"
					id="address"
					bind:value={address}
					class="form-input"
					class:error={errors.address}
					placeholder="Введите адрес ресторана"
				/>
				{#if errors.address}
					<span class="form-error">{errors.address}</span>
				{/if}
			</div>

			<div class="form-group">
				<label for="comment" class="form-label">Комментарий</label>
				<textarea
					id="comment"
					bind:value={comment}
					class="form-textarea"
					placeholder="Дополнительная информация (необязательно)"
				></textarea>
			</div>

			<button type="submit" class="btn btn-primary">Отправить заявку</button>
		</form>
	{/if}
</div>

<style>
	.form-container {
		max-width: 600px;
		margin: 0 auto;
		padding: var(--spacing-xl);
	}

	.form-container h2 {
		text-align: center;
		margin-bottom: var(--spacing-md);
	}

	.form-description {
		text-align: center;
		color: var(--color-text-light);
		margin-bottom: var(--spacing-xl);
	}

	.restaurant-form {
		display: flex;
		flex-direction: column;
	}

	.required {
		color: var(--color-error);
	}

	.form-input.error,
	.form-textarea.error {
		border-color: var(--color-error);
	}

	.form-success {
		text-align: center;
		padding: var(--spacing-xl);
		background-color: #d1fae5;
		border-radius: var(--border-radius);
		color: #065f46;
	}

	.form-success h3 {
		color: #065f46;
		margin-bottom: var(--spacing-md);
	}

	.form-success p {
		margin-bottom: 0;
	}

	@media (max-width: 768px) {
		.form-container {
			padding: var(--spacing-md);
		}
	}
</style>
