<script>
	let mode = 'broke';
</script>

<div class="flex flex-col items-center" style="margin-top:-50px;">
	<img src="cat.png" alt="" />
	<div id="minter" class="flex flex-col gap-4 border-2 rounded-xl p-5">
		<div class="group border-2 rounded-xl p-4">
			<div>Ticker</div>
			<input type="text" class="mt-2 w-full px-1" value="MEW" />
		</div>
		<div class="group border-2 rounded-xl p-4" style="border-color: var(--cl-gray);">
			<div>Total Supply</div>
			<input type="text" class="mt-2 w-full px-1" value="50,000,000,000" />
		</div>
		<div>+ Add Socials</div>

		<div class="group w-full options p-4 flex flex-col gap-2">
			<div class="ml-2">Selected Plan</div>
			<div class="ml-2">I am broke, just mint the token please!</div>
			<div class="w-full flex justify-between">
				<button
					class:selected={mode == 'broke'}
					on:click={() => {
						mode = 'broke';
					}}
				>
					<div class="text-xl">1ERG</div>
					<div class="text-sm">broke</div>
				</button>
				<button
					class:selected={mode == 'classic'}
					on:click={() => {
						mode = 'classic';
					}}
				>
					<div class="text-xl">5ERG</div>
					<div class="text-sm">classic</div>
				</button>
				<button
					class:selected={mode == 'supreme'}
					on:click={() => {
						mode = 'supreme';
					}}
				>
					<div class="text-xl">20ERG</div>
					<div class="text-sm">supreme</div>
				</button>
			</div>
		</div>

		<button class="btn rounded-xl mt-8">mint</button>
	</div>
</div>

<style lang="postcss">
	.group {
		border-color: var(--cl-gray);
		box-shadow: 4px 4px 0px #333;
	}

	.options {
		border: 2px solid #333;
		border-radius: 15px;
		background-color: var(--cl-yellow);
	}
	.options button {
		padding: 4px;
		padding-left: 8px;
		padding-right: 8px;
		cursor: pointer;
	}

	.options .selected {
		border: 2px solid #333;
		border-radius: 12px;
		background-color: white;
	}

	#minter {
		width: 400px;
		background: white;
		border-color: #333;
		border-width: 4px;
		box-shadow: 8px 8px 0px #333;
	}
	img {
		width: 250px;
		margin-bottom: -8px;
		z-index: 1;
	}
</style>
