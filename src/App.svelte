<script>
  import "bulma/css/bulma.min.css";
  import DecimalInput from "./DecimalInput.svelte";
  import BinaryInput from "./BinaryInput.svelte";

  let binary = "";
  let decimal = "";
</script>

<style>
  .center {
    margin: auto;
    width: 50%;
    padding: 10px;
  }
</style>

<nav class="navbar is-primary" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <strong>Binary to Decimal Converter</strong>
    </a>

    <!-- <a
      href="javascript:;"
      role="button"
      class="navbar-burger"
      aria-label="menu"
      aria-expanded="false">
      <span aria-hidden="true" />
      <span aria-hidden="true" />
      <span aria-hidden="true" />
    </a> -->
  </div>
</nav>

<section class="section">
  <div class="container">
    <div class="center">
      <BinaryInput bind:binary bind:decimal />
      <DecimalInput bind:decimal />
    </div>

  </div>
</section>
