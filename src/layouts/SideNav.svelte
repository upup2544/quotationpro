<script>
  import { navigate } from "svelte-routing";

  function createHandleLinkClick(link) {
    return () => {
      navigate(link);
    };
  }

  const navs = [
    ["/home", "Home"],
    ["/quotation", "Quotation"],
    ["/customers", "Customers"],
    ["/web-settings", "Web Settings"],
    ["/archive-box", "Archive Box"],
  ];
</script>

<link
  rel="stylesheet"
  href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css"
  integrity="sha384-r4NyP46KrjDleawBgD5tp8Y7UzmLA05oM1iAEQ17CSuDqnUK2+k9luXQOfXJCJ4I"
  crossorigin="anonymous"
/>

<main>
  <div class="sidenav">
    <div class="company">
      <div>Company Name</div>
    </div>
    <div class="links-container">
      {#each navs as [link, text]}
        <div class="link" on:click="{createHandleLinkClick(link)}">
          <div class="link__icon"></div>
          <div class="link__label">{text}</div>
        </div>
      {/each}
    </div>
  </div>
</main>

<style>
  .sidenav {
    height: 100%; /* 100% Full-height */
    position: relative; /* Stay in place */
  }

  .company {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 4em 0;
  }

  .links-container {
    display: grid;
    gap: 1em;
  }

  .link {
    display: grid;
    grid-template-columns: 2rem 1fr;
    align-items: center;
    gap: 1em;
    cursor: pointer;
  }

  .link__icon {
    width: 100%;
    height: 2rem;
    background-color: white;
    border-radius: 0.5em;
  }
</style>
