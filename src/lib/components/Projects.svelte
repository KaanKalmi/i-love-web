<!-- I don't have any other project I'm proud of to show, so it's rather empty right now -->
<script>
  const Projects = [
    { name: "FDND", link: "https://programma.agency.fdnd.nl/" },
  ];
</script>

<section class="projects">
  <h4 class="section-title">My projects</h4>
    {#each Projects as project}
      <div class="project">
        <a href="{project.link}"> 
          <h3>{project.name}</h3> 
        </a>
          <iframe src={project.link} title="FDND-Programma" height="375" width="575" frameborder="0" loading="lazy" class="phoneBox"></iframe>
      </div>
    {/each}
</section>

<style>

  .projects {
    padding: 4rem 1rem;
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;

      & .project {

        & a {
            text-decoration: none;
            font-size: 1.2rem;
            color: var(--text-color);
            font-weight: 500;
            transition: color var(--transition-speed);

            & h3 {
              font-weight: 400;
              padding-bottom: .25rem;
            }
          }

        & .phoneBox {
          display: inline-flex;
          border-width: 4px;
          border-style: solid;
          border-color:black;
          box-shadow: 0 0 25px 12px var(--hover-color);
          width: 375px;
          height: 575px;
          border-radius: 20px;
          position:relative;
        }
      }
    }

  @media (max-width: 720px) {
    .section-title {
      font-size: 2.5rem;
    }

    .project a {
      font-size: 2.5rem;
    }
  }
</style>