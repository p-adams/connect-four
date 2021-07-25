<script lang="ts">
  const gameboard = [...Array(7)].map((x) => Array(6).fill(""));
  console.log(gameboard);
</script>

<main>
  <h1>Connect Four</h1>
  <div class="gameboard">
    {#each gameboard as col, i}
      <div class="col">
        {#each col as row, j}
          <div class="cell">
            <p>{row}</p>
          </div>
        {/each}
      </div>
    {/each}
  </div>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  .gameboard {
    height: 400px;
    width: 400px;
    background-color: #516dad;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(7, auto);
    grid-template-rows: repeat(6, auto);
    column-gap: 10px;
    row-gap: 10px;
    padding: 12px;
  }

  .cell {
    height: 48px;
    background-color: white;
    border-radius: 100%;
  }
  .cell p {
    vertical-align: middle;
  }
  h1 {
    text-align: center;
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
