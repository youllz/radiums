<script lang="ts">
	import { onMount } from "svelte";
	import { animate, scroll } from "motion";


	onMount(() => {
		if(window.innerWidth > 500) {
			scroll(animate('#contact .line', {scaleY: [1, 0]}, {easing: 'ease-out'}), {
				target: document.querySelector('#contact') as HTMLElement
			})

		}
	}
	
	
)
	
</script>

<section id="contact">
	<p>vous avez un projet ?</p>
	<div class="line"></div>
	<div class="btn-container" >
		<a href="mailto:zyousouf70@gmail.com" >
       discutons-en 
      </a>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		gap: 30px;
		align-items: center;
		justify-content: center;
		padding: 0 5vw;
	}

	.line {
		height: 200px;
		width: 2px;
		background-color: var(--woodsmoke-400);
		transform-origin: top;
	}

	p {
		font-size: clamp(24px, 3vw + 0.1rem, 4rem);
		text-transform: uppercase;
		text-align: center;
	}

	a {
		text-transform: uppercase;
		border-radius: 100vw;
		background-color: var(--woodsmoke-200);
		color: var(--woodsmoke-900);
		padding: 0.7rem 1rem;
    /* position: absolute; */
    position: relative;
    box-shadow: 0 0 20px var(--woodsmoke-200);

    
    /* transform: translate(-50%, -50%); */
	}

  a::before {
    height: 100%;
    width: 100%;
    content: "";
    position: absolute;
   
    border-radius: 100vw;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: all 0.7s var(--easing);

  }

  a:hover::before {
    box-shadow: 0 0 50px var(--woodsmoke-200);
  }

	.btn-container {
		
    display: flex;
    align-items: center;
    justify-content: center;
	}

	@media (width < 500px) {
		.line {
			height: 100px;
			
		}

		section {
			gap: 15px;
		}
	}
</style>
