<!-- <!-- <script>
  export let name = "Your Name";
  export let profileImage = "profile.jpg"; // Make sure this path is correct
</script> -->

<section class="intro">
  <div >
    <!-- <img src={profileImage} alt="{name}'s photo" class="profile-pic" /> -->
  </div>

  <div class="right">
    <!-- <h1>Hi, I'm {name} </h1> -->
    <p>
      I'm a passionate Computer Engineering student with a focus on software development,
      embedded systems, and real-world problem-solving.
    </p>
    <p>
      This portfolio showcases my projects, experiments, and everything in between — from
      full-stack web apps to robotics and IoT systems.
    </p>
    <p>
      Feel free to explore and reach out if you'd like to collaborate or chat tech!
    </p>
  </div>
</section>
.
<style>
  .intro {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    padding: 5rem;
    max-width: 1000px;
    margin: auto;
    gap: 2rem;
  }

  .left {
    flex: 1 1 200px;
    display: flex;
    justify-content: center;
  }

  .right {
    flex: 2 1 400px;
  }

  .profile-pic {
    width: 200px;
    height: 200px;
    object-fit: cover;
    border-radius: 50%;
    border: 4px solid #ccc;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  }

  h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }

  p {
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 1rem;
    color: #444;
  }

  @media (max-width: 768px) {
    .intro {
      flex-direction: column;
      text-align: center;
    }

    .right {
      padding: 0 1rem;
    }
  }
</style>