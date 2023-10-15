<script>
	export let close;
</script>

<div
	class="shadow m-0 fixed top-0 prose dark:prose-invert z-10 flex
        justify-between border p-4 h-fit dark:border-gray-600
        border-gray-400 bg-gray-200 dark:bg-gray-800 right-0 rounded-b-xl"
>
	<div class="flex items-center mx-auto">
		<h3 class="px-4">A.I. Mastery course out now!</h3>
		<br />
		<p>
			If you want to have any chance of not loosing your job to robots, sign up for our A.I. mastery
			course for a limited time deal of <strong>only $199.99</strong>
			<span class=" text-xs dark:text-gray-700 text-gray-300">a week</span>
			(<strong>50% off</strong>)
		</p>
		<button on:click={() => close()}>
			<p class="text-xs text-gray-500 hover:underline dark:hover:text-gray-300 hover:text-gray-700">
				x
			</p>
		</button>
	</div>
</div>
