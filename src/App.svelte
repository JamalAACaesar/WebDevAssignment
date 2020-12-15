<script>
	export let name;

	const logo = "/logo.png";

	const cover =
		"https://unsplash.com/photos/6SMF42-JTAc/download?force=true&w=1920";

	const heroText = "Welcome to Caesar's Gourmet";
	const heroDesc = "Where your every sweet tooth desire will be fulfilled!";
	// const heroDesc = "Here are Caesar's Gourmet, we make the finest deserts for people to not just fulfil their sweet tooth desire, but fill their stomach with our pastries."

	const gallery = [
		{
			src:
				"https://unsplash.com/photos/aFMylf801v0/download?force=true&w=1920",
			price: 20,
			name: 'Glazed Hazel Nut Squash Cake',
			desc: "Sprinkle Delight Donuts with the extra sweet taste are one of our finest creations!",
		},
		{
			src:
				"https://unsplash.com/photos/F71ZHHBYs3w/download?force=true&w=1920",
			price: 15,
			name: 'Apple Cinnamon Cheese Cake',
			desc: "Quadruple Treat Sprnkles offer different donuts with different tastes for you to share with your friends",
		},
		{
			src:
				"https://unsplash.com/photos/vdx5hPQhXFk/download?force=true&w=1920",
			price: 10,
			name: 'Double Choco Rock Cake',
			desc: "Vanilla Choco Cheese Cake is one of the most chosen for couples, here's a hint, get it for her birthday.",
		},
		{
			src:
				"https://unsplash.com/photos/sxIVqaksdfE/download?force=true&w=1920",
			price: 24,
			name: 'Honey Garlic Sweet Cheese Cake',
			desc: "Coconut Shaving Sprinkle",
		},
		{
			src:
				"https://unsplash.com/photos/cKJ8ZxQ2bC8/download?force=true&w=1920",
			price: 7,
			desc: "Random Description",
		},
		{
			src:
				"https://unsplash.com/photos/FtWQhwpe1qc/download?force=true&w=1920",
			price: 5,
			desc: "Random Description",
		},
		{
			src:
				"https://unsplash.com/photos/hV1gChgMa-k/download?force=true&w=1920",
			price: 5.25,
			desc: "Random Description",
		},
		{
			src:
				"https://unsplash.com/photos/pKXH6nqeZtg/download?force=true&w=1920",
			price: 9.3,
			desc: "Random Description",
		},
	];

	const CADFormat = (price) =>
		new Intl.NumberFormat("en-US", {
			style: "currency",
			currency: "CAD",
		}).format(price);
</script>

<style>
	:root {
		--my-color: #ac72ac;
		--dark-color: #f8f8f8;
	}

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
		content: "";
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
		font-family: "Montserrat", sans-serif;
	}

	#hero .info p {
		margin-top: 0.7em;

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

	#grid .picture img {
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
		#grid .picture img {
			width: 100%;
			max-height: 75vh;
			min-width: 0;
		}
	}

	#sec2 {
		background-color: var(--dark-color);
	}

	footer {
		padding: 3em 0;

		text-align: center;

		font-family: "Nunito", sans-serif;

		color: white;
		background-color: var(--my-color);
	}

	footer hr {
		margin: 2em 0;
	}

	footer p {
		/* font-size: 1.2rem; */

		/* text-transform: uppercase; */
	}

	footer i {
		font-size: 1.25em;
	}

	footer .contacts {
		display: grid;
		grid-auto-flow: column;
		justify-content: space-evenly;
	}

	footer .contacts .item {
		position: relative;
		display: flex;
	}

	footer .contacts .item i {
		display: flex;
		align-items: center;
		margin-right: 1.3em;
	}

	footer .contacts .item .inner > p:first-of-type {
		/* color: rgba(0,0,0, 0.7); */
		font-size: 0.8rem;
		text-transform: uppercase;
	}

	footer .contacts .item p {
		text-align: start;
	}

	footer .socials {
		margin-bottom: 1em;
		/* display: flex; */
	}

	footer .socials li {
		display: inline-block;
		margin: 0 0.5em;
		list-style: none;
	}
	footer .socials li a {
		color: inherit;
	}

	#grid .picture {
		position: relative;
		height: 100%;
	}

	#grid .picture .details {
		color: white;
	}

	#grid .picture .details h2 {
		font-size: 1.5rem;
		font-weight: bolder;
	}

	#grid .picture .details p {
		font-size: 1.3rem;
	}

	#grid .picture:hover .details {
		opacity: 1;
		pointer-events: all;
	}

	#grid .picture::before {
		content: "";

		width: 0%;
		height: 100%;

		top: 0;
		left: 0;
		position: absolute;

		opacity: 0;

		background: var(--my-color);

		/* will-change: opacity; */
		transition: all 400ms ease-in-out;
	}

	#grid .picture:hover::before {
		width: 100%;
		opacity: 0.65;
	}

	#grid .picture .details {
		top: 50%;
		left: 50%;

		position: absolute;
		transform: translate(-50%, -50%);

		opacity: 0;
		pointer-events: none;

		text-align: center;

		will-change: opacity;
		transition: opacity 400ms ease-in-out;
	}

	table {
		background:  #ac72ac;
		width: 300px;
		height: 200px;

		margin: 0 auto;
		border-collapse: collapse;
	}

	td, th {
		border: 1px solid white;
		padding: 0.5rem;
		text-align: center;
		color: white;
	}
</style>

<div class="wrapper">
	<header>
		<nav class="menu">
			<div class="logo"><img src={logo} alt="Logo" /></div>

			<ul>
				<li><a href="#hero">Home</a></li>
				<li><a href="#gallery">Gallery</a></li>
			</ul>
		</nav>

		<div id="hero">
			<img src={cover} alt="" srcset="" />

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
							<div class="picture">
								<img src={pic.src} alt="Picture {index + 1}" />

								<div class="details">
									<h2>{CADFormat(pic.price)}</h2>
									<p>{pic.desc}</p>
								</div>
							</div>
						</li>
					{/each}
				</ul>
			</div>
		</section>

		<section id="sec2">
			<div class="container">
				<div class="headline">
					<h2>Today's Specials</h2>
					<p style="text-align: center; margin-bottom: 20px; font-family: Poppins, sans-serif;"> Order one of our special desserts for just today!</p>
				</div>

				<table>
					<thead>
					  <tr>
						<th>#</th>
						<th>Item</th>
						<th>Price</th>
					  </tr>
					</thead>
					<tbody>
					  {#each gallery.slice(0, 4) as item, index (index)}
						<tr>
							<td>{index + 1}</td>
							<td>{item.name}</td>
							<td>{CADFormat(item.price)}</td>
						</tr>
					  {/each}
					  <!-- <tr>
						<td>Brownies</td>
						<td>{CADFormat(5)}</td>
					  </tr>
					  <tr>
						<td>Donuts</td>
						<td>{CADFormat(5)}</td>
					  </tr> -->
					</tbody>
				  </table>
			</div>
		</section>
	</main>

	<footer id="footer">
		<div class="container">
			<div class="contacts">
				<div id="phone" class="item">
					<i class="fas fa-phone" />
					<div class="inner">
						<p>Call Us</p>
						<p>+1 902-999-9999</p>
					</div>
				</div>

				<div id="email" class="item">
					<i class="fas fa-envelope" />
					<div class="inner">
						<p>Email</p>
						<p>me@example.com</p>
					</div>
				</div>

				<div id="address" class="item">
					<i class="fas fa-map-marker-alt" />
					<div class="inner">
						<p>Address</p>
						<p>401 Street, City, CA</p>
					</div>
				</div>
			</div>

			<hr />

			<ul class="socials">
				<li>
					<a
						href="https://facebook.com/xjay.anferneex"
						target="_blank">
						<i class="fab fa-facebook" />
					</a>
				</li>

				<li>
					<a href="https://instagram.com/raseac_kn" target="_blank">
						<i class="fab fa-instagram" />
					</a>
				</li>

				<li>
					<a
						href="https://linkedin.com/in/jamalcaesar"
						target="_blank">
						<i class="fab fa-linkedin" />
					</a>
				</li>
			</ul>

			<p>Copyright &copy; Caesar's Gourmet</p>
		</div>
	</footer>
</div>
