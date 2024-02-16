<script>
    /*** @type {string}*/
    export let text;
    /*** @type {string}*/
    export let link;
</script>

<button>
    <a href={link} target="_blank">{text}</a>
</button>

<style>
    button {
        all: unset;
        background-color: hsl(0, 0%, 20%);
        border-radius: 0.4em;
        color: hsl(0, 0%, 100%);
        padding-block: 1em;
        padding-inline: 6em;
        text-align: center;
    }

    button:hover,
    button:focus,
    button:focus-within {
        background-color: hsl(75, 94%, 57%);
        color: hsl(0, 0%, 8%);
        cursor: pointer;
        transition:
            color 1.5s ease,
            background-color 1.5s ease;
    }

    a {
        color: inherit;
        font-family: "Inter", sans-serif;
        font-weight: 600;
        text-decoration: none;
    }
</style>
