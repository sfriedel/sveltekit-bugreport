<script context="module">
	export const load = async () => ({ props: {} });

</script>

<script>
	import { session } from '$app/stores';

	if (!import.meta.env.SSR) {
		$session.test = 'foo';
	}

</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

$session.test: {$session.test}
