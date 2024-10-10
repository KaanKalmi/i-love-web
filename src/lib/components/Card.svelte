<section class="projects">
    <article>
        Hier komt project 1
    </article>
    <article>
        Hier komt project 2
    </article>
    <article>
        Hier komt project 3
    </article>
</section>

<style>
    .projects{
        display: flex;
        flex-direction: column;
        align-items: center;
        position: absolute;
        top: 60%;
        margin-bottom: 1.5em;

        & article{
            border: 1px solid var(--sec-color);
            height: 18em;
            width: 18em;
            margin-block: 2em;
        }
    }
</style>