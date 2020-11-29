<script>
	export let name;

	const logo = "/logo.png"

	const cover = "https://unsplash.com/photos/6SMF42-JTAc/download?force=true&w=1920"

	const heroText = "Welcome to Caesar's Gourmet"
	const heroDesc = "Where your every sweet tooth desire will be fulfilled!"
	// const heroDesc = "Here are Caesar's Gourmet, we make the finest deserts for people to not just fulfil their sweet tooth desire, but fill their stomach with our pastries."

	const gallery = [
		"https://unsplash.com/photos/aFMylf801v0/download?force=true&w=1920",
		"https://unsplash.com/photos/F71ZHHBYs3w/download?force=true&w=1920",
		"https://unsplash.com/photos/vdx5hPQhXFk/download?force=true&w=1920",
		"https://unsplash.com/photos/sxIVqaksdfE/download?force=true&w=1920",
		"https://unsplash.com/photos/cKJ8ZxQ2bC8/download?force=true&w=1920",
		"https://unsplash.com/photos/FtWQhwpe1qc/download?force=true&w=1920",
		"https://unsplash.com/photos/hV1gChgMa-k/download?force=true&w=1920",
		"https://unsplash.com/photos/pKXH6nqeZtg/download?force=true&w=1920",
	]
</script>

<style>
	section {
		padding: 2.5em 0;
	}

	section .headline h2 {
		padding: 0 0 1em;

		font-size: 1.85rem;
		text-align: center;
		font-family: "Poppins", sans-serif;

		letter-spacing: 3px;
		text-transform: uppercase;
	}

	/* MENU START */
	.menu {
		margin: 1em;

		left: 0;
		right: 0;
		z-index: 10;
		position: absolute;

	    display: flex;
		height: 60px;
		justify-content: space-between;
	}

	.menu .logo {
		display: flex;
		align-items: center;
	}

	.menu .logo img {
	    height: 2.5em;
	    object-fit: contain;
	}

	@media (max-width: 768px) {
		#hero {
			height: 100vh;
		}
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
		color: #fff;
		text-decoration: none;
		font-family: "Nunito", sans-serif;
	}

	@media (max-width: 768px) {
		.menu ul li a {
			font-size: 0.85rem;
		}
	}

	.menu ul li a:hover {
		font-weight: bold;
	}

	/* MENU END */

	/* HERO START */

	#hero {
		position: relative;
		height: 50vh;


		background-color: rgba(34, 34, 34, 0.55);
		border-bottom: 1px solid rgba(0, 0, 0, 0.25);
	}

	@media (max-width: 768px) {
		#hero {
			height: 100vh;
		}
	}

	@media (max-width: 768px) and (max-height: 420px) {
		#hero {
			height: 100vh;
		}
	}

	#hero:before {
		content: '';
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		position: absolute;
		background-color: rgba(34, 34, 34, 0.65);
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
		transform: translateY(-50%);

		text-align: center;
	}

	#hero .info h1 {
		color: #fff;
		font-size: 30px;
		letter-spacing: 1.5px;
		text-transform: uppercase;
		text-decoration: underline;
		font-family: 'Montserrat', sans-serif;
	}

	#hero .info p {
		margin-top: .7em;

		color: #fff;
		font-size: 20px;
		font-family: "Nunito", sans-serif;
		word-wrap: break-word;
	}

	@media (max-width: 540px) {
		#hero .info h1 {
			font-size: 1.3rem;
		}
	}

	/* HERO END */

	#gallery { 
		/* background-color: #E7D7F4; */
	}

	#grid {
		display: flex;
		flex-wrap: wrap;
	}

	#grid li {
		height: 40vh;
		flex-grow: 1;
	}

	#grid li:last-child {
		flex-grow: 10;
	}

	#grid img {
		max-height: 100%;
		min-width: 100%;
		object-fit: cover;
		vertical-align: bottom;
		box-shadow: -2px 2px 10px 0px #ccc;
	}

	@media (max-aspect-ration: 1/1) {
		#grid li {
			height: 30vh;
		}
	}

	@media (max-height: 480px) {
		#grid li {
			height: 80vh;
		}
	}

	@media (max-aspect-ratio: 1/1) and (max-width: 480px) {
		#grid {
			flex-direction: row;
		}

		#grid li {
			height: auto;
			width: 100%;
		}
		#grid img {
			width: 100%;
			max-height: 75vh;
			min-width: 0;
		}
	}

	footer {
		padding: 3em 0;

		text-align: center;

		font-family: "Nunito", sans-serif;

		background-color: #fff;
	}

	footer p {
		/* font-size: 1.2rem; */

		/* text-transform: uppercase; */
	}

	footer i {
		font-size: 1.25em;
	}

	footer .socials {
		margin-top: 1em;
		/* display: flex; */
	}

	footer .socials li {
		display: inline-block;
	    margin: 0 .5em;
		list-style: none;

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
			</ul>
		</nav>

		<div id="hero">
			<img src="{cover}" alt="" srcset="">

			<div class="info">
				<h1>{heroText}</h1>
				<p>{heroDesc}</p>
			</div>
		</div>
	</header>

	<main>
		<section id="gallery">
			<div class="container">
				<div class="headline">
					<h2>Our Popular Dishes</h2>
				</div>
	
				<ul id="grid">
					{#each gallery as pic, index (index)}
						<li>
							<img src="{pic}" alt="Picture {index + 1}">
						</li>
					{/each}
				</ul>
			</div>
		</section>
	</main>


	<footer id="footer">
		<div class="container">
			<p>Copyright &copy; Caesar's Gourmet</p>

			<ul class="socials">
				<li>
					<a href="https://facebook.com/" target="_blank">
						<i class="fab fa-facebook"></i>
					</a>
				</li>

				<li>
					<a href="https://instagram.com/" target="_blank">
						<i class="fab fa-instagram"></i>
					</a>
				</li>

				<li>
					<a href="https://linkedin.com/" target="_blank">
						<i class="fab fa-linkedin"></i>
					</a>
				</li>
			</ul>
		</div>
	</footer>
</div>
