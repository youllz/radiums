<script lang="ts">
	import { animate, inView } from "motion";
	import { onMount } from "svelte";

  const services = [
    {
      name: 'Developpement',
      desc: 'Notre travail consiste à concevoir des produits et des expériences qui incarnent les solutions dont votre marque a besoin.',
      items: ['Developpement Web', 'Optmisation Web', 'Support & management']
    },
    {
      name: 'Digital Design',
      desc: "Un design digital soigné et intuitif améliore l'expérience utilisateur, favorisant l'engagement et fidélisant les visiteurs.",
      items: ['Branding', 'UI/UX Design']
    },
    {
      name: 'Strategie',
      desc: 'Des plans stratégiques soigneusement conçus pour maximiser votre impact numérique et atteindre vos objectifs commerciaux.',
      items: ['Google ads', 'Facebook ads', 'Media Content Marketing']
    },
  ]

  onMount(() => {
    inView('.services-header p:nth-child(2)', (info) => {
      animate(info.target, {opacity: [0, 1], y: [50, 0]}, {duration: 1, easing: 'ease-out', delay: 0.5})
    })
  })
</script>





<section class="services" id="services">
  <div class="services-header">
    <p class="label">
      avec quoi ?
    </p>

    <p>
      Des solutions modernes, concrètes qui ont impact significatif sur les résultats de votre entreprise
    </p>
  </div>

  <div class="service-container">
    {#each services as service}
    <div class="card">
        <div>
          <span>
            {service.name}
          </span>
        </div>
        <div>
          <p class="desc">
            {service.desc}
          </p>
        </div>
        <div>
          <ul>
            {#each service.items as item}
              <li>
                <span>
                  {item}
                </span>
              </li>
            {/each}
          </ul>
        </div>
      </div>
      {/each}
  </div>
</section>


<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 5rem;
    
  }

  .services-header {
    display: flex;
    flex-direction: column;
    gap: 32px;
    max-width: 50%;
  }

  .services-header p:nth-child(1) {
    text-transform: uppercase;
  }

  .service-container {
    display: grid;
    gap: 16px;
  }

  .card {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-auto-rows: minmax(20rem, 1fr);
    border-top: 2px solid var(--woodsmoke-500);
    padding: 20px 0;
    gap: 30px;
  }

  .desc {
    font-size: clamp(18px, 1.5vw + 0.1rem, 2rem);
  }

  ul {
    display: grid;
    gap: 16px;
  }

  @media (width < 700px) {
    .card {
      grid-template-columns: 1fr;
      grid-auto-rows: minmax(5rem, 1fr);
      gap: 16px;
      padding: 50px 0;
    }

     .services-header {
      max-width: 100%;
     }
  }
</style>