<script>
  export let decimal = "";
</script>

<div class="field">
  <label class="label">Decimal Number</label>
  <div class="control has-icons-left has-icons-right">
    <input
      class="input is-success"
      type="text"
      placeholder="Result"
      bind:value={decimal}
      readonly />
    <span class="icon is-small is-left">
      <i class="fas fa-file" />
    </span>
  </div>
</div>
