<script>
  export let image;
  export let title;
  export let description;
</script>

<div class="card">
  <img src={image} alt={title} />
  <div class="card-content">
    <h2 class="card-title">{title}</h2>
    <p class="card-description">{description}</p>
  </div>
</div>

<style>
  .card {
    background-color: var(--red);
    border: 1px solid var(--pink);
    border-radius: 10px;
    overflow: hidden;
    width: 300px;
    box-shadow: 0 4px 12px rgb(180, 65, 103);
    margin: 20px;
    text-align: center;
  }

  .card img {
    width: 100%;
    height: 425px;
    border-radius: 10px;
    border-style: double;
    border-color: var(--light-pink);
  }

  .card-content {
    padding: 15px;
  }

  .card-title {
    font-size: 1.5em;
    color: var(--light-pink);
    margin: 0 0 10px 0;
  }

  .card-description {
    font-size: 1em;
    color: var(--light-pink);
    margin: 0;
  }
</style>
