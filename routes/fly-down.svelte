<script>
	import { fly } from 'svelte/transition';
</script>

<div transition:fly={{ y: -100, duration: 300 }}>
	<slot />
</div>
