<script>
	export let name;

	const logo = "https://brainrain.com.ua/wp-content/uploads/2016/11/intel-company-logo-png-hd-sk.png"

	const cover = "https://unsplash.com/photos/6SMF42-JTAc/download?force=true&w=1920"

	const heroText = "Welcome to Our Gourmet Restaurant"

	const gallery = [
		"https://unsplash.com/photos/aFMylf801v0/download?force=true&w=1920",
		"https://unsplash.com/photos/F71ZHHBYs3w/download?force=true&w=1920",
		"https://unsplash.com/photos/vdx5hPQhXFk/download?force=true&w=1920",
		"https://unsplash.com/photos/sxIVqaksdfE/download?force=true&w=1920",
		"https://unsplash.com/photos/cKJ8ZxQ2bC8/download?force=true&w=1920",
		"https://unsplash.com/photos/FtWQhwpe1qc/download?force=true&w=1920",
		"https://unsplash.com/photos/hw5kIbrdmBc/download?force=true&w=1920",
		"https://unsplash.com/photos/pKXH6nqeZtg/download?force=true&w=1920",
	]
</script>

<style>
	section .headline h2 { 
		font-size: 1.85rem;
		text-align: center;
		font-family: "Poppins", sans-serif;

		letter-spacing: 2px;
		text-transform: uppercase;
	}

	/* MENU START */
	.menu {
	    display: flex;
	    height: 60px;

	    /* background: #ccc; */
	}

	.menu .logo img {
	    height: 100%;
	    object-fit: contain;
	}

	.menu ul {
		display: grid;
		grid-auto-flow: column;

		place-items: center;
	}

	.menu ul li {
	    margin: 0 1em;
	    list-style: none;
	}

	.menu ul li a {
		text-decoration: none;
	}

	/* MENU END */

	/* HERO START */

	#hero {
		position: relative;
		height: 60vh;


		background-color: rgba(34, 34, 34, 0.55);
		border-bottom: 1px solid rgba(0, 0, 0, 0.25);
	}

	#hero:before {
		content: '';
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		position: absolute;
		background-color: rgba(34, 34, 34, 0.55);
	}

	/* #hero .preview {
		height: 100%;
	} */

	#hero img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	#hero .info {
		margin: 0 6em;
	
		left: 0;
		right: 0;
		top: 50%;

		position: absolute;

		text-align: center;
	}

	#hero .info h1 {
		color: #fff;
		font-size: 1.8rem;
		text-transform: uppercase;
		font-family: 'Montserrat', sans-serif;
	}

	@media (max-width: 540px) {
		#hero .info h1 {
			font-size: 1.3rem;
		}
	}

	/* HERO END */

	#gallery .grid {
		display: grid;
		grid: auto-flow dense auto / repeat(auto-fit, minmax(300px, 1fr));
	}

	#gallery .image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	@media (min-width: 640px) {
	}
</style>


<div class="wrapper">
	<header>
		<nav class="menu">
			<div class="logo">
			<img src="{logo}" alt="Logo">
			</div>

			<ul>
				<li>
					<a href="#hero">Home</a>
				</li>
				<li>
					<a href="#gallery">Gallery</a>
				</li>
				<li>
					<a href="#contact">Contact</a>
				</li>
			</ul>
		</nav>

		<div id="hero">
			<img src="{cover}" alt="" srcset="">

			<div class="info">
				<h1>{heroText}</h1>
			</div>
		</div>
	</header>

	<main>
		<section id="gallery">
			<div class="container">
				<div class="headline">
					<h2>Our Gallery</h2>
				</div>
	
				<div class="grid">
					{#each gallery as pic, index (index)}
						<div class="image">
						<img src="{pic}" alt="Picture {index + 1}">
						</div>
					{/each}
				</div>
			</div>
		</section>

		<section id="contact"></section>
	</main>

	<footer>

	</footer>
</div>
