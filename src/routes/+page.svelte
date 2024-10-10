<script>
    import Intro from '$lib/components/Intro.svelte';
    import Cards from '$lib/components/Card.svelte';
</script>

<Intro />

<main>
    <h1> Scroll Down</h1>
    <Cards />
</main>


<style>
    /* Algemene styling */
    main {
        position: absolute;
        top: 25vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        width: 100%;
        overflow-y: auto;
        z-index: 1;
    }
</style>