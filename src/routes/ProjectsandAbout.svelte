<script>
  // Sample project data
  let projects = [
    {
      title: "Smart Home Automation",
      description: "A system using Arduino and sensors to automate home devices.",
      image: "/images/home-automation.jpg",
      link: "https://github.com/yourusername/smart-home"
    },
    {
      title: "Portfolio Website",
      description: "Built using Svelte to showcase my skills and projects.",
      image: "/images/portfolio.png",
      link: "https://yourwebsite.com"
    }
  ];
</script>

<section class="main-container">
  <div class="left-column">
    <h2>🧠 About Me</h2>
    <p>
      I'm a passionate Computer Engineering student with a love for coding, hardware projects,
      and building real-world solutions. I enjoy working on embedded systems, web applications,
      and integrating sensors with microcontrollers. This portfolio is a snapshot of my technical journey.
    </p>
    <p>
      Outside of tech, I enjoy learning new skills, exploring open-source, and sharing ideas with the community.
    </p>
  </div>

  <div class="right-column">
    <h2>🚀 Projects</h2>
    <div class="projects-grid">
      {#each projects as project}
        <div class="project-card">
          <img src={project.image} alt={project.title} />
          <h3>{project.title}</h3>
          <p>{project.description}</p>
          <a href={project.link} target="_blank">View Project 🔗</a>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .main-container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    padding: 2rem;
    max-width: 1200px;
    margin: auto;
  }

  .left-column, .right-column {
    flex: 1 1 500px;
  }

  h2 {
    font-size: 2rem;
    margin-bottom: 1rem;
  }

  .left-column p {
    font-size: 1.1rem;
    line-height: 1.6;
    color: #444;
    margin-bottom: 1rem;
  }

  .projects-grid {
    display: grid;
    gap: 1.5rem;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  }

  .project-card {
    background: #fff;
    border-radius: 1rem;
    padding: 1rem;
    box-shadow: 0 6px 12px rgba(0,0,0,0.05);
    text-align: center;
  }

  .project-card img {
    width: 100%;
    height: 150px;
    object-fit: cover;
    border-radius: 0.75rem;
    margin-bottom: 1rem;
  }

  .project-card h3 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
  }

  .project-card p {
    font-size: 1rem;
    color: #555;
    margin-bottom: 1rem;
  }

  .project-card a {
    text-decoration: none;
    color: white;
    background: #0070f3;
    padding: 0.5rem 1rem;
    border-radius: 0.5rem;
    font-weight: bold;
    transition: background 0.2s ease;
  }

  .project-card a:hover {
    background: #0051a8;
  }

  @media (max-width: 768px) {
    .main-container {
      flex-direction: column;
    }
  }
</style>
