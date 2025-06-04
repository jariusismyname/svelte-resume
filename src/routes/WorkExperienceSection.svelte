<script>
  export let experiences = [
    {
      role: "MSSQL Scripting",
      company: "D&L Idustries, Inc.",
      year: "Summer 2024",
      description: "Developed responsive web applications using Svelte, integrated REST APIs, and collaborated with UX designers to improve user experience."
    },
    {
      role: "Microsoft Power BI Reporter",
      company: "D&L Idustries, Inc.",
      year: "Summer 2024",
      description: "Developed responsive web applications using Svelte, integrated REST APIs, and collaborated with UX designers to improve user experience."
    },
    {
      role: "Intern Software Engineer",
      company: "D&L Idustries, Inc.",
      year: "Summer 2024",
      description: "Assisted in building internal tools using JavaScript and Node.js, fixed bugs, and wrote unit tests for critical components."
    }
  ];
</script>

<section class="experience-section">
  <h2>Work Experience</h2>
  <div class="experience-list">
    {#each experiences as exp}
      <div class="experience-item">
        <h3>{exp.role}</h3>
        <h4>{exp.company} <span class="year">({exp.year})</span></h4>
        <p>{exp.description}</p>
      </div>
    {/each}
  </div>
</section>
<style>
  .experience-section {
    background-color: white;
    padding: 3rem 9rem;
    text-align: left;
  }

  .experience-section h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
    color: #333;
  }

  .experience-list {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    max-width: 800px;
    margin: 0 auto;
  }

  .experience-item {
    background: #f9f9f9;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
    text-align: left;
  }

  .experience-item h3 {
    margin: 0;
    font-size: 1.2rem;
    color: #2e7d32;
  }

  .experience-item h4 {
    margin: 0.5rem 0;
    font-size: 1rem;
    color: #555;
  }

  .experience-item .year {
    font-weight: normal;
    color: #888;
  }

  .experience-item p {
    margin-top: 0.5rem;
    color: #666;
  }

  @media (max-width: 768px) {
    .experience-section {
      padding: 2rem;
    }
  }

  @media (max-width: 600px) {
    .experience-item {
      text-align: center;
    }
  }

  @media (max-width: 480px) {
    .experience-section {
      padding: 1.5rem 1rem;
    }
  }
</style>
