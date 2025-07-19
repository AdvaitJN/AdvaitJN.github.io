<script lang="ts">
	import Button from './Button.svelte';

	let name = '';
	let email = '';
	let subject = '';
	let message = '';
	let sent = false;

	function handleSubmit(e: Event) {
		e.preventDefault();
		sent = true;
		// Reset the form
		name = '';
		email = '';
		subject = '';
		message = '';
	}
</script>

<form class="contact-form" on:submit={handleSubmit} autocomplete="off">
	<div>
		<label for="name">Your Name</label>
		<input id="name" type="text" bind:value={name} required placeholder="Enter your name" />
	</div>
	<div>
		<label for="email">Your Email</label>
		<input id="email" type="email" bind:value={email} required placeholder="Enter your email" />
	</div>
	<div>
		<label for="subject">Subject</label>
		<input id="subject" type="text" bind:value={subject} required placeholder="Subject" />
	</div>
	<div>
		<label for="message">Message</label>
		<textarea id="message" bind:value={message} required placeholder="Type your message here..."
		></textarea>
	</div>
	<Button type="submit" disabled={!name || !email || !subject || !message}>Send Message</Button>

	{#if sent}
		<div class="sent-msg">Thank you! I will reply as soon as possible.</div>
	{/if}
</form>

<style>
	.contact-form {
		max-width: 430px;
		margin: 0 auto;
		display: flex;
		flex-direction: column;
		gap: 1.1rem;
	}

	.contact-form label {
		color: #fff;
		font-weight: 600;
		margin-bottom: 0.2rem;
		display: block;
	}

	.contact-form input,
	.contact-form textarea {
		width: 100%;
		padding: 0.75rem;
		border-radius: 0.75rem;
		border: 1.5px solid #444;
		background: #181716;
		color: #fff;
		font-size: 1rem;
		margin-top: 0.15rem;
		outline: none;
		resize: none;
		box-sizing: border-box;
		transition: border-color 0.2s;
	}
	.contact-form input:focus,
	.contact-form textarea:focus {
		border-color: #ce872a;
	}

	.contact-form textarea {
		min-height: 130px;
		max-height: 320px;
		font-family: inherit;
		font-size: 1rem;
	}

	.sent-msg {
		color: #ce872a;
		font-weight: 600;
		margin-top: 1rem;
		text-align: center;
	}
</style>
