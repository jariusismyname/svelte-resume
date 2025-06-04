<script>
  export let testimonials = [
    {
      name: "Microsoft Power BI Reporter",
      photo: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/New_Power_BI_Logo.svg/900px-New_Power_BI_Logo.svg.png?20210102182532",
      rating: 5,
      text: "Developed responsive web applications using Svelte, integrated REST APIs, and collaborated with UX designers to improve user experience."
    },
    {
      name: "MSSQL Scripting",
      photo: "https://brandlogos.net/wp-content/uploads/2025/03/microsoft_sql_server-logo_brandlogos.net_wykhq-768x768.png",
      rating: 5,
      text: "Developed responsive web applications using Svelte, integrated REST APIs, and collaborated with UX designers to improve user experience."
    },
    {
      name: "Intern Software Engineer",
      photo: "https://a0.anyrgb.com/pngimg/1834/10/source-code-cascading-style-sheets-firm-programmer-software-developer-computer-programming-html-web-development-directory-icon-design.png",
      rating: 5,
      text: "Assisted in building internal tools using JavaScript and Node.js, fixed bugs, and wrote unit tests for critical components."
    }
  ];

  const maxStars = 5;
</script>

<h1 class="testimonial-title">Experiences</h1>

<section class="testimonial-section">
  {#each testimonials as t}
    <div class="testimonial-card">
      <img src={t.photo} alt={"Photo of " + t.name} />
      <h3>{t.name}</h3>
      <div class="stars">
        {#each Array(maxStars) as _, i}
          {#if i < t.rating}
            <span class="star filled">★</span>
          {:else}
            <span class="star">☆</span>
          {/if}
        {/each}
      </div>
      <p>{t.text}</p>
    </div>
  {/each}
</section>

<style>
  .testimonial-title {
    padding: 40px 150px;
    text-align: left;
    font-weight: 700;
    color: #333;
  }

  .testimonial-section {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
    padding: 2rem;
    background: white;
  }

  .testimonial-card {
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgb(0 0 0 / 0.1);
    width: 280px;
    padding: 1.5rem;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .testimonial-card img {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 1rem;
    border: 3px solid #4caf50;
  }

  .testimonial-card h3 {
    margin: 0.5rem 0;
    font-size: 1.2rem;
    color: #333;
  }

  .stars {
    margin: 0.5rem 0;
  }

  .star {
    font-size: 1.5rem;
    color: #ccc;
    margin: 0 2px;
  }

  .star.filled {
    color: #ffc107; /* gold */
  }

  .testimonial-card p {
    font-style: italic;
    color: #555;
    margin-top: 0.5rem;
  }
</style>
