<script>
  const skills = [
    { name: 'GitHub', icon: 'fa-brands fa-github' },
    { name: 'HTML5', icon: 'fa-brands fa-html5' },
    { name: 'CSS3', icon: 'fa-brands fa-css3-alt' },
    { name: 'JavaScript', icon: 'fa-brands fa-js-square' },
    { name: 'Node.js', icon: 'fa-brands fa-node-js' },
    { name: 'Express.js', icon: 'fa-brands fa-express-js' },
    { name: 'SvelteKit', icon: 'fa-brands fa-sveltekit' },
  ];
</script>
  
<section class="skills">
  <h3 class="section-title">My skills</h3>
  <ul class="skill">
    {#each skills as skill}
      <li>
        <i class={skill.icon}></i>
        <p>{skill.name}</p>
      </li>
    {/each}
  </ul>
</section>
  
<style>
  .skills {
    padding: 4rem 8rem;
    margin: 0 auto;
    text-align: center;

      & .skill {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        list-style-type: none;
        gap: 4rem;
        padding: 1rem;
        transition: transform var(--transition-speed), box-shadow var(--transition-speed);
        cursor: pointer;
        text-align: center;
        width: 100%;
        height: 100%;
        pointer-events: none;

        & li {
          padding: 2rem;
          border-radius: 12px;
          pointer-events: all;
        }

        & li i {
          font-size: var(--icon-size);
          color: var(--primary-color);
          margin-bottom: 1rem;
          transition: color var(--transition-speed);
        }
        
        & li p {
          font-size: 1.2rem;
          color: var(--text-color);
          font-weight: 500;
          transition: color var(--transition-speed);
        }
      }
    }
  
  .skill li:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.15);
    background-color: var(--hover-color);
  }
  
  @media (max-width: 720px) {
    .section-title {
      font-size: 2.5rem;
    }
  
    .skill i {
      font-size: 2.5rem;
    }
  }
</style>