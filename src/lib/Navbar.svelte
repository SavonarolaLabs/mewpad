<script lang="ts">
	import Kitty from './Kitty.svelte';
</script>

<div
	class="w-full bg-yellow shadow-bot px-4 rounded-xl flex justify-between items-center"
	style="min-height:100px; border-color: #333; border-width: 4px;"
>
	<div class="text-2xl flex items-center brand-font" style="font-size:40px">
		<Kitty></Kitty>
		<div class="mb-2 ml-1" style="color:#f586b9">mewpad</div>
	</div>

	<div class="flex items-center gap-6">
		<div class="active">Mint</div>
		<div>Burn</div>
		<div>Pool</div>
		<div>FAQ</div>
	</div>

	<div class="active mr-2" style="box-shadow: 6px 6px 0 #f586b9;">Connect Wallet</div>
</div>

<style>
	.active {
		border: 2px solid var(--cl-gray);
		border-radius: 12px;
		padding: 8px;
		padding-left: 12px;
		padding-right: 12px;
		box-shadow: 2px;
		background: white;
		box-shadow: 4px 4px 0 #33333367;
	}
</style>
