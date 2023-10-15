<script>
	export let close;
</script>

<div class="grid items-center justify-center fixed w-screen h-screen">
	<div
		class="dark:bg-gray-800
        bg-gray-200 w-6/12 sm:w-9/12 h-fit prose dark:prose-invert text-center p-3
        rounded-xl mx-auto"
	>
		<br />
		<h1 class="text-6xl dark:text-blue-300 text-blue-800">404</h1>
		<p>Oops! The page you are looking for does not exist. It might have been moved or deleted.</p>
		<button class=" text-gray-500 hover:underline" on:click={close}>close</button>
	</div>
</div>
