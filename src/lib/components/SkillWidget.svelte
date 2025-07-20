<script>
	export let imgSrc;
	export let name;
	export let color = '#ce872a';
	export let onClick = () => {};
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div class="card" on:click={onClick} style="--accent-color: {color}">
	<img class="logo" src={imgSrc} alt={name + ' logo'} />
	<div class="name">{name}</div>
</div>

<style>
	.card {
		min-width: 6rem;
		min-height: 6rem;
		width: auto;
		height: auto;
		background: var(--background-color);
		border-radius: 1rem;
		box-shadow: 0 4px 24px 0 rgba(0, 0, 0, 0.4);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		cursor: pointer;
		transition: box-shadow 0.2s;
	}

	.card:hover,
	.card:focus-visible {
		border: 2px solid var(--secondary-color);
		box-shadow: 0 6px 24px rgba(206, 135, 42, 0.18);
		z-index: 1;
	}
	.logo {
		max-width: 70%;
		max-height: 70%;
		/* margin-bottom: 16px; */
		user-select: none;
		pointer-events: none;
	}
	.name {
		color: var(--accent-color);
		font-weight: bold;
		font-size: 1rem;
		text-align: center;
	}
</style>
