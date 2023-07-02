<style>
	.blok {
		width: 1152px;
		background-color: #fff;
		border-radius: 7px;
		margin-left: 64px;
	}
	.raspisanie {
		background: url(Raspisanie.jpg);
		width: 900px;
		height: 1260px;
		z-index: 1;
		margin-left: 120px;
	}
	.custom-checkbox {
		position: absolute;
		z-index: -1;
		opacity: 0;
	}
	h1 {
		border-radius: 7px;
		border: 1px solid black;
		text-align: center;
		cursor: default;
	}
	label {
		margin-left: 80px;
		border: 1px solid black;
		border-radius: 4px;
	}
</style>

<script>
	import { fade } from 'svelte/transition';
	let visible = true;
</script>

<div class="blok">
	<h1>Расписание занятий</h1>
	<label>
		<input type="checkbox" class="custom-checkbox" bind:checked={visible}/>
		Расписание на Июнь 2023г.
	</label>
	
	{#if visible}
			<div class="raspisanie" transition:fade>1</div>
	{/if}
</div>