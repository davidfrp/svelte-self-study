<script>
    export let posts = [];
</script>

<ul>
    {#each posts as {author, message, sentAt, likes}}
        <li>
            <date>{sentAt.toLocaleString()}</date>
            {#if message.trim().length > 0}
                <p>{message}</p>
            {:else}
                <p>
                    <strong>No message</strong>
                </p>
            {/if}
        </li>
    {/each}
</ul>

<style>
    ul {
        list-style: none;
        padding: 0;
    }

    li {
        margin-bottom: 1em;
    }

    date {
        font-size: 0.8em;
    }

    p {
        margin: 0;
    }
</style>
