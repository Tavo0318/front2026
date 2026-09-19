```svelte
<svelte:head>
	<title>Cuidemos nuestro planeta</title>
	<meta
		name="description"
		content="Conozcamos, protejamos y aprovechemos responsablemente nuestros recursos naturales."
	/>
</svelte:head>

<div class="page">
	<main class="card">
		<section class="content">
			<div class="badge">Naturaleza y conservación</div>

			<h1>Cuidemos nuestro planeta 🌎</h1>

			<p class="intro">
				Conozcamos, protejamos y aprovechemos responsablemente nuestros
				recursos naturales.
			</p>

			<div class="buttons">
				<a href="#recursos" class="primary">Conocer más</a>
				<a href="#acciones" class="secondary">¿Qué podemos hacer?</a>
			</div>
		</section>

		<section class="illustration" aria-label="Ilustración de la naturaleza">
			<div class="sun"></div>
			<div class="cloud cloud-one"></div>
			<div class="cloud cloud-two"></div>
			<div class="mountain mountain-one"></div>
			<div class="mountain mountain-two"></div>
			<div class="tree tree-one">
				<div class="trunk"></div>
				<div class="leaves"></div>
			</div>
			<div class="tree tree-two">
				<div class="trunk"></div>
				<div class="leaves"></div>
			</div>
		</section>
	</main>

	<section id="recursos" class="info">
		<h2>Nuestros recursos naturales</h2>
		<p>
			El agua, el aire, los bosques y la biodiversidad son esenciales para
			la vida. Cuidarlos es responsabilidad de todos.
		</p>
	</section>

	<section id="acciones" class="info">
		<h2>Pequeñas acciones, grandes cambios</h2>
		<p>
			Podemos ahorrar agua y energía, reducir residuos, reciclar y
			proteger los espacios naturales.
		</p>
	</section>
</div>

<style>
	:global(body) {
		margin: 0;
		font-family:
			Arial, Helvetica, sans-serif;
		background: #eef7ef;
		color: #173b2b;
	}

	.page {
		min-height: 100vh;
		padding: 40px 20px;
		box-sizing: border-box;
	}

	.card {
		max-width: 1100px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: 1fr 1fr;
		background: white;
		border-radius: 28px;
		overflow: hidden;
		box-shadow: 0 15px 40px rgba(23, 59, 43, 0.12);
	}

	.content {
		padding: 70px 55px;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.badge {
		display: inline-block;
		width: fit-content;
		padding: 8px 14px;
		border-radius: 30px;
		background: #dff2df;
		color: #287443;
		font-size: 14px;
		font-weight: bold;
		margin-bottom: 20px;
	}

	h1 {
		font-size: clamp(42px, 6vw, 70px);
		line-height: 1;
		margin: 0 0 25px;
		color: #185c37;
	}

	.intro {
		font-size: 20px;
		line-height: 1.6;
		color: #557062;
		max-width: 550px;
	}

	.buttons {
		display: flex;
		gap: 14px;
		flex-wrap: wrap;
		margin-top: 25px;
	}

	.buttons a {
		text-decoration: none;
		padding: 14px 20px;
		border-radius: 12px;
		font-weight: bold;
	}

	.primary {
		background: #287443;
		color: white;
	}

	.secondary {
		border: 2px solid #287443;
		color: #287443;
	}

	.illustration {
		min-height: 500px;
		position: relative;
		overflow: hidden;
		background: linear-gradient(#bde8f5 0%, #e9f7d5 68%, #7fbe63 68%);
	}

	.sun {
		position: absolute;
		width: 100px;
		height: 100px;
		border-radius: 50%;
		background: #ffd76a;
		top: 65px;
		right: 80px;
	}

	.cloud {
		position: absolute;
		background: white;
		border-radius: 50px;
		width: 130px;
		height: 38px;
	}

	.cloud::before,
	.cloud::after {
		content: "";
		position: absolute;
		background: white;
		border-radius: 50%;
	}

	.cloud::before {
		width: 55px;
		height: 55px;
		left: 20px;
		bottom: 5px;
	}

	.cloud::after {
		width: 45px;
		height: 45px;
		right: 20px;
		bottom: 4px;
	}

	.cloud-one {
		top: 100px;
		left: 60px;
	}

	.cloud-two {
		top: 170px;
		right: 30px;
		transform: scale(0.7);
	}

	.mountain {
		position: absolute;
		bottom: 160px;
		width: 0;
		height: 0;
		border-left: 170px solid transparent;
		border-right: 170px solid transparent;
		border-bottom: 230px solid #5c9960;
	}

	.mountain-one {
		left: -70px;
	}

	.mountain-two {
		right: -80px;
		border-bottom-color: #467d53;
	}

	.tree {
		position: absolute;
		bottom: 40px;
	}

	.tree-one {
		left: 90px;
		transform: scale(1.1);
	}

	.tree-two {
		right: 100px;
		transform: scale(0.8);
	}

	.trunk {
		width: 28px;
		height: 115px;
		background: #765134;
		margin: 0 auto;
		border-radius: 8px;
	}

	.leaves {
		width: 150px;
		height: 150px;
		background: #2f7d45;
		border-radius: 50%;
		position: absolute;
		bottom: 75px;
		left: -61px;
		box-shadow:
			-45px 20px 0 #3e914f,
			45px 20px 0 #3e914f;
	}

	.info {
		max-width: 1000px;
		margin: 35px auto 0;
		padding: 35px;
		background: white;
		border-radius: 22px;
		box-shadow: 0 8px 25px rgba(23, 59, 43, 0.08);
	}

	.info h2 {
		margin-top: 0;
		color: #185c37;
	}

	.info p {
		line-height: 1.7;
		color: #557062;
	}

	@media (max-width: 800px) {
		.page {
			padding: 20px 12px;
		}

		.card {
			grid-template-columns: 1fr;
		}

		.content {
			padding: 45px 30px;
		}

		.illustration {
			min-height: 400px;
		}
	}
</style>
```
