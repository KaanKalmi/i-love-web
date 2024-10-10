<script>
    import Intro from '$lib/components/Intro.svelte';
    import Cards from '$lib/components/Card.svelte';
</script>

<Intro />

<main>
    <Cards />
</main>


<style>
    /* Algemene styling */
    main {
        position: absolute;
        top: 40vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        width: 100%;
        overflow: hidden;
        z-index: 1;
    }
</style>