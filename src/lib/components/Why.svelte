<script lang="ts">
	import { animate, scroll, stagger } from "motion";
	import { onMount } from "svelte";

  const words =
		`Chez PIXELVi, nous sommes animés par une conviction : aider les entreprises à prospérer dans l'univers numérique en leur offrant une visibilité qui va bien au-delà des clics et des vues.`.split(
			' '
		);


    // onMount(() => {
    //   scroll(animate(
    //     '#why p span', {backgroundSize: ['0%', '100%']}, {delay: stagger(0.1)}
    //   ), {
    //     target: document.querySelector('#why p ') as HTMLElement,

    //     // container:  document.querySelector('#why  ') as HTMLElement
    //   })
    // })
</script>

<section id="why">
  <div class="container">
    <span class="label">
      POURQUOI NOUS 
    </span>
    <!-- <p>
      {#each words as letter}
					<span class="reveal">
						{letter}
					</span>
				{/each}
    </p> -->
    <p>
      <span  class="scroll-reaveal">
        Chez RADIUMS, nous
        sommes animés par
        une conviction : aider
        les entreprises à
        prospérer dans l'univers
        numérique en leur
        offrant une visibilité qui
        va bien au-delà des
        clics et des vues.
      </span>
    </p>
  </div>
</section>


<style>
  section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  

  
  .container {
    display: grid;
    gap: 32px;
   

    & p {
      font-size: clamp(30px, 8vw + 0.1rem, 8rem);
      line-height: 98%;
     
      
      
			/* background-size: 0%; */

      
    }
  }
  
  .scroll-reaveal {
    color: transparent;
  background-size: 0% 100%;
  background-repeat: no-repeat;
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
  color: #3a34464d;
  background-image: linear-gradient(90deg, #f7f6f9, #f7f6f9);
  animation: scroll-reaveal ease-out forwards;
  animation-timeline: view(y);
  animation-range-start: cover 10vh;
  animation-range-end: cover 200vh;
  
  }
  @keyframes scroll-reaveal {
    to {
      background-size: 100% 100%;
    }
  }


  @media (width < 730px) {
    .container {
      max-width: 100%;
    }
  }

  @media (width < 890px) {
    .scroll-reaveal {
      animation-range-end: cover 120vh;
    }
  }
</style>