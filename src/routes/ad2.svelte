<script>
	import { bounceIn } from 'svelte/easing';
	import { scale } from 'svelte/transition';
	let time = 5;
	let expired = false;
	function countdown() {
		if (expired == false) {
			time = Math.max(0, Math.round((time - 0.1) * 10) / 10);
		}
		if (time == 0) {
			expired = true;
		}
	}
	setInterval(countdown, 100);
</script>

<div
	class="rounded sm:mb-10 lg:grid lg:grid-cols-5 md:grid-cols-none lg:h-full prose dark:prose-invert"
>
	<div
		class="dark:bg-slate-800 bg-slate-200 px-10 py-10 max-w-md m-auto lg:col-span-2 mt-20 mb-20 shadow-xl rounded-xl lg:mt-10 md:shadow-xl md:rounded-xl lg:shadow-none lg:rounded-none lg:w-full lg:mb-10 lg:px-5 lg:pt-5 lg:pb-5 lg:max-w-lg"
	>
		<img
			class="h-64 sm:h-52 sm:w-full sm:object-cover lg:hidden object-center mt-2 rounded-lg shadow-2xl"
			src="https://images.pexels.com/photos/1488463/pexels-photo-1488463.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
			alt="Ad:  womens clothing shop"
		/>
		<h2>EPIC DEALS!!!</h2>
		<p class="prose-lead">BUY IT BEFORE IT'S TOO LATE!!!</p>
		<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
			labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
			laboris nisi ut aliquip ex ea commodo consequat.
		</p>
		<p class="font-bold prose-lead text-xl">Deals expire in: {time} seconds!!!</p>
		{#if expired}
			<p in:scale={{ easing: bounceIn }} class="text-5xl font-extrabold text-red-600">EXPIRED!!!</p>
		{/if}
		<button
			class="mt-5 bg-gray-600 p-3 shadow-2xl rounded-full text-white font-bold hover:bg-gray-800"
			>BUY! BUY!! BUY!!!</button
		>
	</div>

	<div class="hidden relative lg:block lg:col-span-3 rounded">
		<img
			class="absolute inset-0 w-full h-full object-cover object-center"
			src="https://images.pexels.com/photos/1488463/pexels-photo-1488463.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2"
			alt="Ad:  womens clothing shop"
		/>
	</div>
</div>
