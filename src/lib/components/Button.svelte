<script lang="ts">
	export let type: 'button' | 'submit' | 'reset' = 'button';
	export let disabled: boolean = false;
	export let className: string = '';
</script>

<button {type} {disabled} class={`btn ${className}`}>
	<slot />
	<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px"
		><path d="M647-440H160v-80h487L423-744l57-56 320 320-320 320-57-56 224-224Z" /></svg
	>
</button>

<style>
	.btn {
		padding: 1rem 1.5rem;
		border: none;
		border-radius: 1rem;
		background: var(--secondary-color);
		color: var(--background-color);
		font-weight: bold;
		font-size: 1rem;
		cursor: pointer;
		display: flex;
		align-items: center;
		transition: background 0.2s;
		justify-content: center;
	}
	svg {
		color: var(--background-color);
	}
	.btn:disabled {
		background: #aaa;
		cursor: not-allowed;
	}
	.btn:hover:enabled {
		background: #005bb5;
	}
</style>
