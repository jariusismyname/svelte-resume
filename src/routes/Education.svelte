<script>
  export let education = [
    {
      degree: "Bachelor of Science in Computer Engineering",
      institution: "University of Rizal System - Antipolo Campus",
      year: "2021 - 2025",
      description: "Focused on embedded systems, robotics, and software development."
    },
    {
      degree: "NATIONAL CERTIFICATE II in Computer System Servicing",
      institution: "TESDA",
      year: "2025",
      description: "Completed training in computer hardware servicing, including installation, configuration, and troubleshooting of computer systems."
    }
  ];
</script>

<section class="education-section">
  <h2>Education</h2>
  <div class="education-list">
    {#each education as edu}
      <div class="education-item">
        <h3>{edu.degree}</h3>
        <h4>{edu.institution} <span class="year">({edu.year})</span></h4>
        <p>{edu.description}</p>
      </div>
    {/each}
  </div>
</section>

<style>
  .education-section {
    background-color: white;
    padding: 3rem 9rem;
    text-align: left;
  }
@media (max-width: 768px) {
  .education-section {
    padding: 2rem;
  }
}

@media (max-width: 480px) {
  .education-section {
    padding: 1.5rem 1rem;
  }
}
  .education-section h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
    color: #333;
  }

  .education-list {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    max-width: 800px;
    margin: 0 auto;
  }

  .education-item {
    background: white;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    text-align: left;
  }

  .education-item h3 {
    margin: 0;
    font-size: 1.2rem;
    color: #4caf50;
  }

  .education-item h4 {
    margin: 0.5rem 0;
    font-size: 1rem;
    color: #555;
  }

  .education-item .year {
    font-weight: normal;
    color: #888;
  }

  .education-item p {
    margin-top: 0.5rem;
    color: #666;
  }

  @media (max-width: 600px) {
    .education-item {
      text-align: center;
    }
  }
</style>
