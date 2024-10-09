<div class="intro-animation">
    <h1> I LOVE WEB </h1>
</div>

<style>
    .intro-animation {
        display: flex;
        align-items: center;
        width: fit-content;
        margin-inline: auto;
        margin-top: 2em;
    }

    .intro-animation h1 {
        margin: 0 auto;
        letter-spacing: .15em;
        text-decoration: underline;
        text-decoration-color: var(--prim-color);
        text-decoration-thickness: 0.5em;
        text-underline-offset: -.35em;
        text-decoration-skip-ink: none;
        animation: 
            slide-up 2.5s cubic-bezier(0.65, 0, 0.35, 1) forwards;
    }

    @keyframes slide-up {
        0% { height: 100vh; }
        100% { height: 5vh; }
    }
</style>