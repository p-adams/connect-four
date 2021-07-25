<script lang="ts">
</script>

<main>
  <h1>Connect Four</h1>
  <div class="gameboard" />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }
  .gameboard {
    height: 400px;
    width: 400px;
    border: 1px solid black;
    margin: 0 auto;
    display: grid;
  }
  h1 {
    color: cornflowerblue;
    text-transform: uppercase;
    font-size: 3rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }
  }
</style>
