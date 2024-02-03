<!-- TODO: add navbar and background texture -->

<script>
	import styles from './layout.module.scss';

	let navOpen = false;

	let resizeTimer = 0;

	function handleResize() {
		document.body.classList.add('stop-transitions');
		clearTimeout(resizeTimer);
		resizeTimer = setTimeout(() => {
			document.body.classList.remove('stop-transitions');
		}, 600);
	}
</script>

<!-- Navbar -->
<div class={styles['container']}>
	<button
		on:click={() => (navOpen = !navOpen)}
		class={`${styles['mobile-nav-toggle']} ${navOpen ? styles.closeBtn : ''}`}
		aria-controls="primary-navigation"
		aria-expanded="false"><span class="sr-only">Menu</span></button
	>
	<nav>
		<ul
			id="primary-navigation"
			class={`${styles['primary-navigation']} ${navOpen ? styles.open : ''}`}
		>
			<li>
				<a href="/">Home</a>
			</li>
			<li>
				<a href="/music">Music</a>
			</li>
			<li>
				<a href="/store">Store</a>
			</li>
		</ul>
	</nav>
</div>

<!-- Footer -->
<slot />
