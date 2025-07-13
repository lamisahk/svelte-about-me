<!-- src/lib/LinkCard.svelte -->
<script>
  export let icon;
  export let text;
  export let url;
</script>

<style>
  .link-card {
    background-color: #ffffff;
    border: 2px solid #a9cee8;
    border-radius: 12px;
    padding: 1rem;
    text-align: center;
    width: 200px;
    transition: transform 0.3s ease, background-color 0.3s ease;
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    text-decoration: none;
    color: #003a64;
  }

  .link-card:hover {
    transform: translateY(-6px);
    background-color: #e1ecf0; /* var(--baby-blue) equivalent */
  }

  .link-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* Two columns */
  gap: 1.5rem;
  justify-items: center;
}

  a {
    text-decoration: none;
    color: inherit;
  }
</style>

<a href={url} target="_blank" class="link-card">
  <div>{icon} {text}</div>
</a>