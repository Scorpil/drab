<script lang="ts">
	import { Sheet } from "$lib";

	let display = false;
</script>

<button
	type="button"
	class="button button-primary"
	on:click={() => (display = true)}
>
	Open
</button>

<Sheet
	bind:display
	class="z-40 backdrop-blur"
	classSheet="card rounded-none border-none"
	position="r"
>
	<div class="mb-4 flex items-center justify-between">
		<h2 class="my-0">Sheet</h2>
		<button
			type="button"
			class="button button-ghost"
			on:click={() => (display = false)}
		>
			Close
		</button>
	</div>
	<div>
		Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
		quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
		consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
		cillum dolore eu fugiat nulla pariatur.
	</div>
</Sheet>
