<script>
  import LinkCard from "./lib/LinkCard.svelte";
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Merriweather:wght@400;600&family=Poppins:wght@300;400;600&display=swap");

  :global(body) {
    font-family: 'Poppins', sans-serif;
    background-image: url('/svelte-about-me/bg.jpg');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    font-size: 1rem;
    color: #003a64;
    margin: 0;
    padding: 0;
  }

  .container {
    max-width: 800px;
    margin: auto;
    padding: 2rem;
  }

  header {
    text-align: center;
    background-image: url('/svelte-about-me/cloud.jpg');
    background-size: cover;
    background-position: center;
    padding: 3rem;
    border-radius: 20px;
    margin-bottom: 2rem;
    backdrop-filter: blur(4px);
    color: #003a64;
  }

  h1, h2 {
    font-family: "Merriweather", serif;
    color: #003a64;
  }

  section {
  background-color: white;
  border: 1px solid #a9cee8;
  border-radius: 12px;
  padding: 1.5rem;
  margin-bottom: 2rem;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 10px rgba(84, 162, 210, 0.1);
}
  .image-grid {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .image-grid img:hover {
  transform: scale(1.05);
  transition: transform 0.3s ease;
  box-shadow: 0 6px 12px rgba(84, 162, 210, 0.2);
}

.link-card {
  transition: transform 0.3s ease, background-color 0.3s ease;
}

.link-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  justify-items: center;
  max-width: 600px;
  margin: 0 auto;
  padding-top: 1rem;
}

.link-card:hover {
  transform: translateY(-6px);
  background-color: var(--baby-blue);
}

  .image-grid img {
    width: 200px;
    height: 200px;
    object-fit: cover;
    border: 3px solid #a9cee8;
    border-radius: 12px;
    background-color: #fff;
  }

  footer {
    text-align: center;
    font-weight: bold;
    margin-top: 2rem;
    color: #003a64;
  }
</style>

<div class="container">
  <header>
    <h1>Hi! I'm Lamisah 🫶🏻</h1>
    <p>pronounced lah-mee-sah :)</p>
    <p><em>experimenting at the intersection of design and development</em></p>
  </header>

  <section>
    <h2>🫐 About Me 🫐</h2>
    <p>
      I’m a 21-year-old girl, an avid reader and movie/tv show enthusiast who enjoys getting lost in a good story. I’m a proud cat aunt, an occasional writer, and someone who’s always down to explore, build, or create — especially when it gets a little chaotic.
    </p>
  </section>

  <section>
    <h2>Things I 💙</h2>
    <div class="image-grid">
      <img src="/svelte-about-me/emb-bead.jpg" alt="bead embroidery" />      
      <img src="/svelte-about-me/cat.jpg" alt="cute cat" />
      <img src="/svelte-about-me/PW.jpg" alt="watching movies" />
    </div>
  </section>

  <section>
    <h2>💻 My Coding Journey 💻</h2>
    <p>
      I was first introduced to coding in a high school computer science class, but it wasn’t until KWK’s Web Dev camp that I saw what I could actually do with it. That’s when it snowballed, and I realized the possibilities were endless. If something doesn’t exist, you can make it. With code, you can tell stories, build art, and create things that feel like you.
    </p>
  </section>

  <section>
    <h2>Currently Watching 🎬</h2>
    <div class="image-grid">
      <img src="/svelte-about-me/kim-c.jpg" alt="kim's convenience" />
      <img src="/svelte-about-me/sm.png" alt="superman" />
      <img src="/svelte-about-me/spf.png" alt="space force" />
    </div>
  </section>

  <section>
    <h2> 🔗 </h2>
    <div class="link-grid">
      <LinkCard icon="🎧" text="what I'm listening to" url="https://music.apple.com/qa/album/nice-to-each-other/1814620245?i=1814620247" />
      <LinkCard icon="🎬" text="favourite movie" url="https://letterboxd.com/film/pride-prejudice/" />
      <LinkCard icon="🍝" text="comfort recipe" url="https://www.youtube.com/watch?v=psjfRM4m2Rk" />
      <LinkCard icon="🧵" text="embroidery starter" url="https://youtu.be/IqbJe0wBXV0?si=j9qoiLsd3DpaMXFA" />
    </div>
  </section>

  <footer>
    <p>Made with 🩵 by Lamisah</p>
  </footer>
</div>