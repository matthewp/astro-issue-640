<script>
  let count = 0;

  function add() {
    count++;
  }
</script>


<button id="theme-switch" aria-label="Trocar tema" on:click={add}>
  + ({ count })
</button>