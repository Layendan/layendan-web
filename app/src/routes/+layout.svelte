<script lang="ts">
	import '../app.css';
	import Fa from 'svelte-fa';
	import { faGithub, faDiscord, faLinkedin } from '@fortawesome/free-brands-svg-icons';

	let { children } = $props();
</script>

<div class="navbar bg-base-300 sticky top-0 z-50 shadow-sm">
	<div class="navbar-start"></div>
	<div class="navbar-center">
		<a class="btn btn-ghost text-xl" href="/">layendan.dev</a>
	</div>
	<div class="navbar-end gap-1">
		<a
			href="https://github.com/Layendan"
			target="_blank"
			rel="noopener noreferrer"
			class="btn btn-ghost btn-square btn-lg"
		>
			<Fa icon={faGithub} class="w-5! h-5!" />
		</a>
		<a href="discord://-/users/235566430693752832" class="btn btn-ghost btn-square btn-lg">
			<Fa icon={faDiscord} class="w-5! h-5!"/>
		</a>
		<a
			href="https://www.linkedin.com/in/aidan-labourdette/"
			target="_blank"
			rel="noopener noreferrer"
			class="btn btn-ghost btn-square btn-lg"
		>
			<Fa icon={faLinkedin} class="w-5! h-5!"/>
		</a>
	</div>
</div>

{@render children()}
