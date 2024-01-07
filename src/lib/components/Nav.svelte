<script lang="ts">
	import { scrollLenis } from "$lib/store";


</script>



<nav>
  <div class="logo">
    <a href="/">
     {#each ' RADIUMS' as letter}
      <span>
        {letter}
      </span>
     {/each}
    </a>
  </div>

  <ul>
    <li>
      <a  href="#services" on:click={() => {scrollLenis.scrollTo('#services')}}>
        Services
      </a >
    </li>
    <li>
      <a href="#approche">
        Approche
      </a>
    </li>
    <li>
      <a href="#faq">
        Faq
      </a>
    </li>
    <li>
      <a href="#contact">
        Contact
      </a>
    </li>
  </ul>
  <div class="menu">
    <button>
      menu
    </button>
  </div>
</nav>
<div>

</div>

<style>
  nav {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--woodsmoke-150);
    background-color: var(--woodsmoke-600);
    border-radius: 100vw;
    /* padding: 0.2vw; */
    padding: 15px;
  }
  
  ul {
    display: flex;
    /* gap: 20px; */
    /* padding-inline: 5px; */
    background-color: var(--woodsmoke-600);
    border-radius: 100vw;
  }

  li a {
    padding: 10px 1rem;
    border-radius: 100vw;
    font-weight: 500;
    transition:  background-color 0.5s ease-out;
    /* font-size: clamp(20px, 1.2vw + 0.1rem, 2rem); */
  }
  
  a:hover {
    background-color: var(--woodsmoke-400);

  }

  .logo a {
    font-size: clamp(16px, 1.2vw + 0.1rem, 2rem);
    font-weight: 500;
  }
  
  .menu {
    display: none;
  }
  
  .menu button {
    font-size: clamp(16px, 1.2vw + 0.1rem, 2rem);

  }

  @media (width < 750px) {
   .menu {
    display: block;
   }
    
  }

  @media (width < 750px) {
    ul {
      display: none;
    }
  }
</style>