<svelte:head>
	<title>VPC Bratihka</title>
</svelte:head>

<nav>
	<div class="nav-container">
		<div class="nav-links">
			{#each nav as link}
			{#if link.isShow}
				<a href={link.href} class="link">{link.title}</a>
			{/if}
			{/each}
		</div>
	</div>
</nav>
<div class="container">
	<slot></slot>
</div>

<script>
	const nav = [
		{ 
			title: 'О клубе',
			href: '/about',
			isShow: true
		},
		{
			title: 'Новости',
			href: '/new',
			isShow: true
		},
		{
			title: 'Занятия',
			href: '/lessons',
			isShow: true
		},
		{
			title: 'Медиа',
			href: '/media',
			isShow: true
		},
		{
			title: 'Достижения',
			href: '/achievements',
			isShow: true
		},
		{
			title: 'Обратная связь',
			href: '/feedback',
			isShow: true
		},
	]
</script>

<style>
	.container {
		max-width: 1400px;
		margin: 50px auto;
	}
</style>