<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>


<script>
    import { onMount } from 'svelte';
    import { page } from '$app/stores';
    
    onMount(async  () => {
        const res = await (await fetch('http://localhost:3000/health-check')).text()
        console.log(res);
    });
    
    $: console.log('Current page:', $page);
</script>