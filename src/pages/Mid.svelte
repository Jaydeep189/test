<script>
    export let comment;
</script>


<svelte:head>
	<title>MID Page</title>
</svelte:head>

<main>
    <div>
        {#each comment as c}
        <h1>{c.postId}</h1>
        <h1>{c.id}</h1>
        <h1>{c.name}</h1>
        <h1>{c.email}</h1>
        <h1>{c.body}</h1>
        {/each}
    </div>
</main>