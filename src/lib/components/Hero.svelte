





<script>
	import Btn from "./Btn.svelte";

</script>


<section id="acceuil">

	<div class="if">
		<img src="/images/hero-img.png" alt="">
		
	<!-- <div class="hidden"></div> -->

	</div>
	<div class="acceuil-content">
		<div>
			<p>Transformer votre visibilité en succès réel, voilà notre mission.</p>
		</div>
		<div>
			<p>
				<span>
					RADIUMS
				</span> est un studio de design et de technologie. Nous construisons des produits numériques, de zéro
				jusqu'au lancement.
			</p>
			<div><a href="#contact"><Btn/></a></div>
		</div>
	</div>
	<!-- <div class="big-text">
		<p>Transformer votre visibilité en succès réel, voilà notre mission.</p>
	</div>
	<div class="acceuil-bottom">
		<p>
			<span>
        UNDERDOT
      </span> est un studio de design et de technologie. Nous construisons des produits numériques, de zéro
			jusqu'au lancement.
		</p>

    <Btn>
      travailler avec nous
    </Btn>
	</div> -->
</section>

<style>

	/* .hidden {
		position: absolute;
		height: 50px;
		width: 160px;
		background-color: red;
		z-index: 900000000;
		bottom: 2%;
		right: 1%;
		background-color: var(--woodsmoke-950);
	} */

	.if {
		position: relative;
		height: 30rem;

	}
	section {
		display: grid;
		padding: 0 5vw;
		grid-template-columns: 1fr;
		/* grid-auto-rows: minmax(30rem, 1fr); */
		
	}

	.acceuil-content {
		min-height: 50vh;
		width: 100%;
		border-top: 2px solid var(--woodsmoke-500);
		display: grid;
		grid-template-columns: 2fr 1fr;
		padding-block: 20px;
		gap: 30px;
		/* background-color: red; */
	}

	.acceuil-content div:nth-child(1) p {
		font-size: clamp(22px, 5vw, 4rem);
		text-transform: uppercase;
	}
	.acceuil-content div:nth-child(2) p {
	 font-size: clamp(16px, 1.5vw + 0.1rem, 2rem);
	}
	.acceuil-content div:nth-child(2)  {
		display: flex;
		flex-direction: column;
		gap: 32px;
		align-items: flex-start;

	}

	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: top;
	}



	@media (width < 800px) {
    .acceuil-content {
      grid-template-columns: 1fr;
			gap: 16px;
			min-height: auto;
    }

		section {
			justify-content: center;
		}
  }



  
</style>
