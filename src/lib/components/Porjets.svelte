<section>
  <figure>
    <img src="/images/image-1.jpg" alt="">  
  </figure>
  <figure>
    
    <img src="/images/image-2.jpg" alt="">  
  </figure>
</section>

<style>
	section {
    padding: 5vw;
    /* padding-block: 10vw; */
		min-height: 100dvh;
    display: grid;
    gap: 10px;
    grid-template-columns: 1fr 1fr;
	}
  
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 20px;
  }

  @media (width < 800px) {
    section {
      grid-template-columns: 1fr;
    }
  }
</style>
