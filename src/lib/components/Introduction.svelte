<script>
  import pfp from '$lib/images/profilePicture.jpg';
</script>
  
<section class="hero">
  <div class="text-content">
    <h2> Introduction </h2>
    <p class="hero-desc">
      I'm a web developer based in the Netherlands. 
      My goal is to craft high-performing, visually captivating, and highly accessible websites and apps. 
      With a dedication to precision and finesse, I am committed to creating digital experiences that not only impress aesthetically
      but also function seamlessly for all users.
    </p>
  </div>
  <div class="img-cover">
    <img src="{pfp}" alt="" height="250px" width="250px"/>
  </div>
</section>
  
<style>
  .hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    padding: 4rem 10rem 0 0;

    & .text-content {
      flex: 1;
      padding-right: 2rem;
      max-width: 600px;
      white-space: wrap;

      &  h2 {
        font-size: 2.5rem;
        margin: 0 0 1rem;
        color: var(--primary-color);
        white-space: nowrap;
        overflow: hidden;
        width: fit-content;
      }

      & .hero-desc {
        font-size: 1.125rem;
        line-height: 1.6;
        color: var(--text-color);
        margin-top: 1rem;
      }
    }

    & .img-cover {
      height: 250px;
      width: 250px;
      border-radius: 50%;
      border: 0;
      overflow: hidden;
      box-shadow: 0 0 16px var(--hover-color);

      & img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
  
  @media (max-width: 720px) {
    .hero {
      flex-direction: column;
      padding: 2rem 1rem;

      & .text-content {
        padding-right: 0;
        max-width: 100%;
        text-align: center;

        & h2 {
          font-size: 2rem;
        }

        & .hero-desc {
          font-size: 1rem;
          margin-top: 0.5rem;
        }
      }

      & .img-cover {
        margin-top: 1.5rem;
        margin-left: 0;
      }
    }
  }
</style>