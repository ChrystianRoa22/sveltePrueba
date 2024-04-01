<script>
  export let title, poster, year
</script>

<style>
  article {
    border: 1px solid #eee;
    border-radius: 4px;
    padding: 16px;
  }

  h3 {
    font-size: 24px;
    margin-bottom: 4px;
  }
</style>

<article>
  <h3>{title}</h3>
  <img src={poster} alt={title}>
  <span>{year}</span>
  {#if 2020 - year < 5}
    <i>NUEVA</i>
  {/if}
</article>