<script>
	import { onMount } from 'svelte';
	import Dropdown from './Dropdown.svelte';
	import { animate, inView } from 'motion';

	onMount(() => {

		const spans = [...document.querySelectorAll('.faq-left p:nth-child(2) span')]
		inView('#faq', (info) => {
			animate(
				spans,
				{ opacity: [0, 1], y: [50, 0] },
				{ duration: 1, easing: 'ease-out', delay: 0.5 }
			);
		});
	});
</script>

<section id="faq">
	<div class="faq-left">
		<p>FAQ</p>
		<p>
			<span>Réponse rapide</span>
			<span>aux questions </span>
			<span>que vous pourriez avoir</span>
		</p>
	</div>
	<div class="faq-right">
		<Dropdown>
			<p slot="header">Quels types de projets acceptez-vous ?</p>
			<p slot="content">
				Nous travaillons avec une variété de projets, qu'il s'agisse de petites entreprises locales
				ou de grandes entreprises, chacune bénéficiant d'une approche personnalisée adaptée à ses
				besoins.
			</p>
		</Dropdown>
		<Dropdown>
			<p slot="header">Comment démarrer un projet ensemble ?</p>
			<p slot="content">
				Chaque projet est sur-mesure, jusqu'à l'équipe qui sera mobilisée. Il y aura quatre étapes
				pour lancer les choses :
				<br />
				<br />

				1 — Vous nous partagez votre projet et nous définissons votre besoin lors d’un premier
				échange. <br /> <br />2 — RADIUMS analyse la demande et rassemble les talents préssentis
				pour votre équipe projet. <br /> <br /> 3 — Toute l’équipe réalise une roadmap, estime les
				coûts et vous présente son approche et sa stratégie. <br /> <br /> 4 — Convaincus ? Go. Nous
				concrétisons notre collaboration lors d’un premier kickoff !
			</p>
		</Dropdown>

		<Dropdown>
			<p slot="header">Quels sont vos tarifs ?</p>
			<p slot="content">
				Nos tarifs varient en fonction des besoins spécifiques de chaque projet. Nous élaborons des
				propositions sur mesure après une consultation initiale gratuite.
			</p>
		</Dropdown>

		<Dropdown>
			<p slot="header">Quels délais prévoyez-vous pour la réalisation des projets ?</p>
			<p slot="content">
				Les délais dépendent de la complexité et de la taille du projet. Nous établissons des
				calendriers réalistes lors de la planification initiale et nous restons flexibles pour
				ajuster si nécessaire.
			</p>
		</Dropdown>

		<Dropdown>
			<p slot="header">Comment est organisée votre équipe de travail ?</p>
			<p slot="content">
				Notre équipe est constituée d'experts indépendants spécialisés dans différents domaines.
				Cette flexibilité nous permet de constituer des équipes adaptées à chaque projet.
			</p>
		</Dropdown>

		<Dropdown>
			<p slot="header">Comment puis-je suivre l'avancement de mon projet ?</p>
			<p slot="content">
				Nous vous tenons régulièrement informé de l'avancement de votre projet par le biais de mises
				à jour fréquentes, de rapports d'étape et de réunions régulières selon vos préférences.
			</p>
		</Dropdown>
	</div>
</section>

<style>
	section {
		min-height: 100dvh;
		color: var(--woodsmoke-50);
		/* padding: 10vw 5vw; */
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 50px;
	}

	.faq-left p:nth-child(1) {
		font-size: 16px;
		text-transform: uppercase;
		color: var(--text);
		font-weight: 400;
		margin-bottom: 5px;
	}
	.faq-left p:nth-child(2) {
		font-size: clamp(22px, 2vw + 0.1rem, 4rem);
		color: var(--text);
		font-weight: 500;
		/* line-height: 90%; */
		min-height: max-content;
		overflow: hidden;

		& span {
			display: inline-block;
		}
	}

	@media (width < 750px) {
		section {
			grid-template-columns: 1fr;
			gap: 20px;
		}
	}
</style>
