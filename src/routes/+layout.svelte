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

<div class="contayner">
	<div class="hone_rot"></div>
	<div class="rot"></div>
	<div class="cot">
		<h1 class="h1">ВПК "Братишка"</h1>
		<p class="p1">город Ахтубинск, Астраханская область</p>
	</div>
</div>

<div class="container">
	<slot></slot>
</div>
<script>
	const nav = [
		{ 
			title: 'Главная',
			href: '/',
			isShow: true
		},
		{ 
			title: 'Занятия',
			href: '/about',
			isShow: true
		},
		{
			title: 'Медиа',
			href: '/media',
			isShow: true
		},
		{
			title: 'Достижения',
			href: '/lessons',
			isShow: true
		},
		{
			title: 'Контакты',
			href: '/new',
			isShow: true
		}
	]
</script>
<style>
	.container {
		max-width: 1400px;
		margin: 50px auto;
	}
</style>