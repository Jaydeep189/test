<script>
    import {Link} from 'svelte-navigator'
    export let photo;
</script>

<svelte:head>
	<title>Home Page</title>
</svelte:head>

<main>
    <div>
        <Link to="/mid">mid</Link>
        {#each photo as p}
            <h1>{p.albumId}</h1>
            <h1>{p.id}</h1>
            <h1>{p.title}</h1>
            <h1>{p.url}</h1>
            <h1>{p.thumbnailUrl}</h1>
        {/each}
    </div>
</main>