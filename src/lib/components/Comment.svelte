<script>
	import { animate, inView } from "motion";
	import { onMount } from "svelte";

  onMount(() => {
    inView('.comment-texts p:nth-child(2)', (info) => {
      animate(info.target, {opacity: [0, 1], y: [50, 0]}, {duration: 1, easing: 'ease-out', delay: 0.5})
    })
    inView('.comment-texts p:nth-child(3)', (info) => {
      animate(info.target, {opacity: [0, 1], y: [50, 0]}, {duration: 1, easing: 'ease-out', delay: 0.5})
    })
  })
</script>



<section id="comment">
  <div class="comment-left">
    <!-- <p>Des expériences digitales ultra-fluides, pour ceux qui aiment avoir un coup d'avance.</p> -->
    <img src="/images/3d.png" alt="">
  </div>
  <div class="comment-right">
    <div class="comment-texts">
      <!-- <p>Des expériences digitales ultra-fluides, pour ceux qui aiment avoir un coup d'avance.</p> -->
      <p class="label">
        COMMENTS ?
      </p>
      <p>
        Notre approche repose sur une compréhension approfondie de votre entreprise et de vos besoins en ligne. Nous commençons par écouter attentivement votre vision et vos objectifs, puis nous élaborons des stratégies sur mesure. Grâce à une combinaison de gestion de réseaux sociaux, de création de contenu captivant et de techniques de référencement pointues, nous donnons vie à votre présence en ligne.
      </p>
      <p>
        Notre équipe est conçue sur mesure pour chaque projet. Nous collaborons avec des experts indépendants, chacun spécialisé dans son domaine, pour offrir à nos clients une expérience unique.
      </p>
    </div>
  </div>
</section>


<style>
  section {
    /* min-height: 100dvh; */
    display: grid;
    grid-template-columns: 3fr 2fr;
    min-height: 45vw;
    gap: 3rem;
  }

  /* .comment-left p{
    font-size: clamp(30px, 5vw + 0.1rem, 7rem);
    line-height: 98%;
  } */

  .comment-texts {
    display: flex;
    flex-direction: column;
    gap: 32px;
  }

  .comment-right {
    display: flex;
    align-items: flex-end;
    flex-direction: column;
    justify-content: flex-end;
    gap: 16px;
  }

  .comment-left {
    overflow: hidden;
  }

 

  .comment-right p{
    /* margin-top: 5vw; */
    font-size: clamp(15px, 1.1vw + 0.1rem, 16px);
    
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: right;
  }
  


  @media (width < 900px) {
    section {
      grid-template-columns: 1fr;
    }
  }
</style>