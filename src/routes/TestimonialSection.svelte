<script>
  export let testimonials = [
    {
      name: "Alice Johnson",
      photo: "https://randomuser.me/api/portraits/women/68.jpg",
      rating: 5,
      text: "This service was amazing! Highly recommend to everyone."
    },
    {
      name: "Mark Smith",
      photo: "https://randomuser.me/api/portraits/men/45.jpg",
      rating: 4,
      text: "Very good experience, will definitely come back."
    },
    {
      name: "Emily Davis",
      photo: "https://randomuser.me/api/portraits/women/24.jpg",
      rating: 5,
      text: "Absolutely loved it, stars for the quality!"
    }
  ];

  const maxStars = 5;
</script>

<h1 class="testimonial-title">Testimonial</h1>

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
