<script>
  export let binary;
  export let decimal;

  let isValid;
  const regExp = /^[0-1]{1,}$/g;

  $: if (binary.match(regExp)) {
    isValid = true;
    decimal = binary;
  } else {
    isValid = false;
    decimal = "";
  }
</script>

<div class="field">
  <label class="label">Binary Number</label>
  <div class="control has-icons-left has-icons-right">
    <input
      class="input {binary != '' && isValid ? 'is-success' : 'is-danger'}"
      type="text"
      placeholder="Binary to convert(0 or 1)"
      bind:value={binary} />
    <span class="icon is-small is-left">
      <i class="fas fa-calculator" />
    </span>
  </div>
  {#if binary != '' && !isValid}
    <p class="help is-danger">invalid number</p>
  {/if}
</div>
