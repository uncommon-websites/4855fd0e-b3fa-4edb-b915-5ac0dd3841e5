<script lang="ts">
	import type { HTMLAttributes } from "svelte/elements";
	const props: HTMLAttributes<HTMLImageElement> = $props();
</script>

<img src="https://logo.clearbit.com/mercor.com" alt="Mercor" {...props} />
