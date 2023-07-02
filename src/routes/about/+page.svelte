<script>
	import { fade } from 'svelte/transition';
	let visible = true;
</script>

<div class="blok">
	<h1 class="h4">Расписание занятий</h1>
	<label>
		<input type="checkbox" class="custom-checkbox" bind:checked={visible}/>
		Расписание на Июнь 2023г.
	</label>
	
	{#if visible}
			<div class="raspisanie" transition:fade>1</div>
	{/if}
</div>