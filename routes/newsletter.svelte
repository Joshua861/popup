<script type="text/javascript">
	export let close;
	export let subscribe;

	let address = '';
	let valid;
	let regex =
		/^([^\x00-\x20\x22\x28\x29\x2c\x2e\x3a-\x3c\x3e\x40\x5b-\x5d\x7f-\xff]+|\x22([^\x0d\x22\x5c\x80-\xff]|\x5c[\x00-\x7f])*\x22)(\x2e([^\x00-\x20\x22\x28\x29\x2c\x2e\x3a-\x3c\x3e\x40\x5b-\x5d\x7f-\xff]+|\x22([^\x0d\x22\x5c\x80-\xff]|\x5c[\x00-\x7f])*\x22))*\x40([^\x00-\x20\x22\x28\x29\x2c\x2e\x3a-\x3c\x3e\x40\x5b-\x5d\x7f-\xff]+|\x5b([^\x0d\x5b-\x5d\x80-\xff]|\x5c[\x00-\x7f])*\x5d)(\x2e([^\x00-\x20\x22\x28\x29\x2c\x2e\x3a-\x3c\x3e\x40\x5b-\x5d\x7f-\xff]+|\x5b([^\x0d\x5b-\x5d\x80-\xff]|\x5c[\x00-\x7f])*\x5d))*$/g;
	function checkValidity() {
		valid = regex.test(address);
	}
</script>

<div class="fixed h-screen w-screen flex justify-center items-center">
	<div
		class="prose dark:prose-invert shadow m-0 fixed p-4 h-fit
        dark:border-gray-600 border-gray-400 bg-gray-200 dark:bg-gray-800 rounded-xl shadow-xl border border-slate-500"
	>
		<h2>Join our newsletter!</h2>
		<p>Make sure to always be updated with new information!</p>
		<div class="relative mb-3" data-te-input-wrapper-init>
			<input
				type="email"
				name="email"
				bind:value={address}
				class="w-full rounded bg-slate-300 dark:bg-slate-700 px-2"
				on:input={checkValidity}
			/>
		</div>
		{#if valid == false}
			<p class="text-red-700 dark:text-red-400">Email address is invalid.</p>
		{/if}
		{#if valid}
			<p class="text-green-700 dark:text-green-400">Email address is valid.</p>
		{/if}
		<label>
			<input type="checkbox" checked />
			I want to recive marketing information
		</label>
		<br />
		<label>
			<input type="checkbox" checked />
			I want to know how your kids are doing
		</label>
		<br />
		<label>
			<input type="checkbox" checked />
			I want cool cool bug facts
		</label>
		<br /><br />

		<button
			on:click={subscribe}
			class="bg-sky-600 px-3 py-1 mx-1 rounded-lg text-white hover:bg-sky-500 transition-all active:bg-sky-700"
		>
			Subscribe
		</button>
		<button
			on:click={close}
			class="dark:bg-slate-700 px-3 py-1 mx-1 rounded-lg dark:text-slate-300 bg-slate-300 text-slate-700 transition-all hover:translate-x-32 delay-150"
		>
			Close
		</button>
	</div>
</div>
