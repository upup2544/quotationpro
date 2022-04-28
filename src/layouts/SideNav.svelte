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
        ["/archive", "Archive"]
    ];
</script>

<main>
    <div class="sidenav">
        {#each navs as [link, text]}
            <div on:click={createHandleLinkClick(link)}>{text}</div>
        {/each}
    </div>
</main>

<style>
    .sidenav {
        height: 100%; /* 100% Full-height */
        width: 8%; /* 0 width - change this with JavaScript */
        position: fixed; /* Stay in place */
        z-index: 1; /* Stay on top */
        top: 0; /* Stay at the top */
        left: 0;
        background-color: rgb(14, 9, 9); /* Black*/
        /* Disable horizontal scroll */
        padding-top: 60px; /* Place content 60px from the top */
        transition: 0.5s; /* 0.5 second transition effect to slide in the sidenav */
        background-color: white;
    }
</style>
