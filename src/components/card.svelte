<script>
    import Button from "./button.svelte";
    import { links } from "$lib/links";
</script>


<div class="card">
    <div class="card-avatar">
        <img width="80px" height="80px" src="circle.png" alt="avatar">
    </div>
    <div class="card-info">
        <div class="card-name">Fredy Madrid</div>
        <div class="card-location">Santa Rosa de Copan, Honduras</div>
    </div>
    <div class="card-position">"Developer"</div>
    <div class="card-link">
        {#each Object.entries(links) as [text, link]}
            <Button text={text} link={link} /> 
        {/each}
    </div>
</div>

<style>
    * {
        color: hsl(0, 0%, 100%);
        font-family: "Inter", sans-serif;
    }

    .card {
        background-color: hsl(0, 0%, 12%);
        border-radius: 0.7em;
        display: grid;
        gap: 1.7em;
        justify-items: center;
        margin-top: 4em;
        max-width: 355px;
        padding: 1.7em;
    }

    .card-avatar img {
        border-radius: 50%;
    }

    .card-info {
        text-align: center;
    }

    .card-name {
        font-size: 28px;
        font-weight: 600;
    }

    .card-location {
        color: hsl(75, 94%, 57%);
        font-weight: 900;
    }

    .card-link {
        display: grid;
        gap: 1em;
    }
</style>