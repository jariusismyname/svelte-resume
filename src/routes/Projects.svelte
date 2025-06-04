<script>
  export let projects = [
    {
      title: "Smart Home Automation",
      description: "A system using Arduino and sensors to automate lights, fans, and monitor temperature remotely.",
      image: "/images/home-automation.jpg",
      link: "https://github.com/yourusername/smart-home"
    },
    {
      title: "Portfolio Website",
      description: "My personal web portfolio built using Svelte, showcasing my projects and skills.",
      image: "/images/portfolio.png",
      link: "https://yourwebsite.com"
    },
    {
      title: "RC Car Controlled via Web App",
      description: "An RC car project using Wi-Fi control, live sensor feedback, and a custom-built dashboard.",
      image: "/images/rc-car.jpg",
      link: "#"
    }
  ];
</script>

<section class="projects">
  <h2> My Projects</h2>

  <div class="projects-grid">
    {#each projects as project}
      <div class="project-card">
        {#if project.image}
          <img src={project.image} alt={project.title} />
        {/if}

        <h3>{project.title}</h3>
        <p>{project.description}</p>

        {#if project.link}
          <a href={project.link} target="_blank" rel="noopener">View Project 🔗</a>
        {/if}
      </div>
    {/each}
  </div>
</section>

<style>
  .projects {
    padding: 3rem 2rem;
    max-width: 1200px;
    margin: auto;
  }

  h2 {
    text-align: left;
    font-size: 2.5rem;
    margin-bottom: 2rem;
  }

  .projects-grid {
    display: grid;
    gap: 2rem;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  }

  .project-card {
    background: #fff;
    border-radius: 1rem;
    padding: 1.5rem;
    box-shadow: 0 8px 16px rgba(0,0,0,0.08);
    transition: transform 0.3s ease;
    text-align: center;
  }

  .project-card:hover {
    transform: translateY(-5px);
  }

  .project-card img {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 0.75rem;
    margin-bottom: 1rem;
  }

  .project-card h3 {
    font-size: 1.4rem;
    margin-bottom: 0.5rem;
  }

  .project-card p {
    font-size: 1rem;
    color: #555;
    margin-bottom: 1rem;
  }

  .project-card a {
    display: inline-block;
    text-decoration: none;
    background: #0070f3;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    font-weight: bold;
    transition: background 0.2s ease;
  }

  .project-card a:hover {
    background: #0058cc;
  }
</style>
