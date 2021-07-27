<script lang="ts">
  const gameboard = [...Array(7)].map((x) => Array(6).fill(""));
  let turn = 0;
  function handleCellClick(col: number, row: number) {
    if (gameboard[col][row] === "") {
      turn++;
      gameboard[col][row] = turn;
      return;
    }
    console.log("filled cell");
  }
  // TODO: implement function to determine if move is a winning move
  function isWinningMove() {}
</script>

<main>
  <h1>Connect Four</h1>
  <div class="gameboard">
    {#each gameboard as col, colIndex}
      <div class="col">
        {#each col as row, rowIndex}
          <div
            class={`cell ${
              row !== "" ? (row % 2 !== 0 ? "fill-x" : "fill-y") : "empty"
            }`}
            on:click={() => handleCellClick(colIndex, rowIndex)}
          >
            <p />
          </div>
        {/each}
      </div>
    {/each}
  </div>
</main>

<style lang="scss">
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
    column-gap: 10px;
    row-gap: 10px;
    padding: 12px;
  }

  .cell {
    height: 48px;
    background-color: white;
    border-radius: 100%;
    p {
      vertical-align: middle;
    }
    &.fill-x {
      background-color: red;
    }
    &.fill-y {
      background-color: yellow;
    }
    &.empty {
      &:hover {
        box-shadow: 0 0 15px green;
        cursor: pointer;
      }
    }
    &:hover {
      box-shadow: inset 0 0 2px black;
    }
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
