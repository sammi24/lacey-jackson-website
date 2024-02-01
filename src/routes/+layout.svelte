<!-- TODO: add navbar and background texture -->

<script>
	import './styles/layout.scss';
	import './styles/global.scss';
</script>

<!-- Navbar -->
<div class="container flex">
	<nav class="flex">
		<ul class="flex">
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
