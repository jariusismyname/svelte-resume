<script>

  import { onMount } from 'svelte';

  let name = '';
  let email = '';
  let feedback = '';
  let rating = 0;
  let submitted = false;
  let error = '';

  const maxStars = 5;

  function submitFeedback() {
    error = '';

    if (!name.trim() || !email.trim() || !feedback.trim() || rating === 0) {
      error = 'Please fill all fields and give a rating.';
      return;
    }
    // Here you can handle sending feedback to a backend or API
    // For now, we'll just simulate submission:
    submitted = true;

    // Reset form fields if you want
    name = '';
    email = '';
    feedback = '';
    rating = 0;
  }
</script>

<section class="feedback-section">
  <h2>Website Feedback</h2>
  
  {#if submitted}
    <p class="thank-you">Thanks for your feedback! We appreciate your honesty.</p>
  {:else}
    <form on:submit|preventDefault={submitFeedback}>
      <label>
        Name:
        <input type="text" bind:value={name} placeholder="Your name" />
      </label>

      <label>
        Email:
        <input type="email" bind:value={email} placeholder="Your email" />

      <!-- <label for="feedback">Your Feedback:</label>

        <div class="stars">
        {#each Array(maxStars) as _, i}
  <button
    type="button"
    class="star {i < rating ? 'filled' : ''}"
    aria-label="Rate {i + 1} star{i === 0 ? '' : 's'}"
    on:click={() => rating = i + 1}
  >★</button>
{/each}


        </div>
      </label> -->
<div></div>
      <label>
        Your Feedback:
<textarea id="feedback" bind:value={feedback} placeholder="Tell us what you think..."></textarea>
      </label>

      {#if error}
        <p class="error">{error}</p>
      {/if}

      <button type="submit">Submit Feedback</button>
    </form>
  {/if}
</section>

<style>
  .feedback-section {
    max-width: 500px;
    margin: 2rem auto;
    background: #fefefe;
    padding: 2rem;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    font-family: sans-serif;
  }

  h2 {
    text-align: center;
    margin-bottom: 1.5rem;
  }

  label {
    display: block;
    margin-bottom: 1rem;
    font-weight: 600;
  }

  input[type="text"],
  input[type="email"],
  textarea {
    width: 100%;
    padding: 0.6rem;
    margin-top: 0.3rem;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 1rem;
  }

  textarea {
    min-height: 100px;
    resize: vertical;
  }

  .stars {
    margin-top: 0.5rem;
  }

  .star {
  background: none;
  border: none;
  padding: 0;
}


  .star.filled {
    color: #f39c12; /* gold */
  }

  button {
    background-color: #333;
    color: white;
    border: none;
    padding: 0.8rem 1.5rem;
    border-radius: 8px;
    cursor: pointer;
    font-weight: 700;
    font-size: 1rem;
    width: 100%;
  }

  button:hover {
    background-color: #555;
  }

  .error {
    color: #e74c3c;
    font-weight: 600;
    margin-top: -0.5rem;
    margin-bottom: 1rem;
  }

  .thank-you {
    text-align: center;
    font-size: 1.2rem;
    font-weight: 600;
    color: #27ae60;
  }
</style>
