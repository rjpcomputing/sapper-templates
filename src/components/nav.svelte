<script>
	export let segment;
	let isBurgerMenuActive = false;

	function ShowMenu( /*params*/ ) {
		isBurgerMenuActive = !isBurgerMenuActive;
	}
</script>

<nav class="navbar is-link" role="navigation" aria-label="main navigation">
	<div class="navbar-brand">
		<a class="navbar-item" href>
			<img alt="Logo" src="/logo-192.png" height="28">
		</a>

		<a href on:click|preventDefault="{ShowMenu}" class:is-active="{isBurgerMenuActive}" role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="app-navbar-menu">
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
		</a>
	</div>

	<div id="app-navbar-menu" class:is-active="{isBurgerMenuActive}" class="navbar-menu">
		<div class="navbar-start" >
			<a href="." class:is-active="{segment === undefined}" class="navbar-item">
				Home
			</a>

			<a href="about" class:is-active="{segment === 'about'}" class="navbar-item">
				About
			</a>

			<a href="blog" class:is-active="{segment === 'blog'}" class="navbar-item">
				Blog
			</a>
		</div>

		<div class="navbar-end">
			<div class="navbar-item">
				<div class="buttons">
					<a href class="button is-primary">
						<strong>Log in</strong>
					</a>
				</div>
			</div>
		</div>
	</div>
</nav>
