<script>
	export let close;
	export let more;
</script>

<div class="fixed mx-3 z-10 bg-gray-200 dark:bg-gray-800 p-3 rounded-lg top-20">
	<div class="prose dark:prose-invert">
		<h3>Support Free Content</h3>
		<p>
			We work day and night, to make these top tier articles <strong>JUST FOR YOU</strong>!!! And
			this is how you repay us? By using an ad blocker? Disgraseful (i dont forgive easily).
		</p>
	</div>
	<br />
	<button
		on:click={() => more()}
		id="disable-adblock"
		class="bg-blue-500 dark:hover:bg-blue-300 hover:bg-blue-400 transition dark:bg-blue-400 p-1 rounded-lg px-2"
		>How to disable ad blocker</button
	><br />
	<button id="keep-stealing" class="text-xs text-gray-400 hover:underline" on:click={() => close()}>
		keep on stealing our hard work
	</button>
</div>
