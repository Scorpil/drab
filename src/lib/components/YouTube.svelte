<!--
@component

### YouTube

Embeds a YouTube video `iframe` into a website with the video `uid`, using [www.youtube-nocookie.com](https://support.google.com/youtube/answer/171780?hl=en#zippy=%2Cturn-on-privacy-enhanced-mode).

@props

- `autoplay` - auto-plays the video
- `class` 
- `id` 
- `start` - start time (seconds)
- `title` 
- `uid` - unique YouTube id

@example

```svelte
<script lang="ts">
	import { YouTube } from "drab";
</script>

<YouTube
	class="aspect-video w-full rounded"
	title="Renegade - Kevin Olusola"
	uid="gouiY85kD2o"
/>
```
-->

<script lang="ts">
	let className = "";
	export { className as class };

	export let id = "";

	/** unique YouTube id */
	export let uid: string;

	export let title = "";

	/** auto-plays the video */
	export let autoplay = false;

	/** start time (seconds) */
	export let start = 0;
</script>

<iframe
	class={className}
	{id}
	src="https://www.youtube-nocookie.com/embed/{uid}?start={start}{autoplay
		? '&autoplay=1'
		: ''}"
	{title}
	frameborder="0"
	allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
	allowfullscreen
/>
