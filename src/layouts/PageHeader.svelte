<script>
  export let path;
  export let title;
</script>

<div class="header">
  <div class="header__path">{path}</div>
  <div class="header__title">{title}</div>
</div>

<style>
  .header {
    display: grid;
    gap: 0.5em;
    padding: 2rem 0;
  }

  .header__path {
    color: grey;
    font-size: small;
  }

  .header__title {
    font-weight: bold;
    font-size: x-large;
  }
</style>