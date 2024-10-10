<script>
    import gsap from 'gsap';
    import { onMount } from 'svelte';

    onMount(() => {
        gsap.from('.clip-top, .clip-bottom', {
            duration: 2,
            delay: 1,
            height: '50vh',
            ease: 'power4.inOut',
        });

        gsap.to('.marquee', {
            duration: 3.5,
            delay: 0.75,
            top: '50%',
            ease: 'power4.inOut',
        });

        gsap.from('.clip-top .marquee, .clip-bottom .marquee', {
            duration: 5,
            delay: 1,
            left: `100%`,
            ease: 'power3.inOut',
        });

        gsap.from('.clip-center .marquee', {
            duration: 5,
            delay: 1,
            left: `-50%`,
            ease: 'power3.inOut',
        });

        gsap.to('.clip-top', {
            duration: 2,
            delay: 6,
            clipPath: 'inset(0 0 100% 0)',
            ease: 'power4.inOut',
        });

        gsap.to('.clip-bottom', {
            duration: 2,
            delay: 6,
            clipPath: 'inset(100% 0 0 0)',
            ease: 'power4.inOut',
        });

        gsap.to('.clip-top .marquee , .clip-bottom .marquee, .clip-center .marquee span', {
            duration: 1,
            delay: 6,
            opacity: 0,
            ease: 'power4.inOut',
        });
    });
</script>

<section class="loader">
    <div class="loader-clip clip-top">
        <div class="marquee">
            <div class="marquee-container">
                <span> I </span>
                <span> I </span>
                I
                <span> I </span>
                <span> I </span>
            </div>
        </div>
    </div>
    <div class="loader-clip clip-bottom">
        <div class="marquee">
            <div class="marquee-container">
                <span> WEB </span>
                <span> WEB </span>
                WEB
                <span> WEB </span>
                <span> WEB </span>
            </div>
        </div>
    </div>
    <div class="clip-center">
        <div class="marquee">
            <div class="marquee-container">
                <span> ❤️ </span>
                <span> ❤️ </span>
                ❤️
                <span> ❤️ </span>
                <span> ❤️ </span>
            </div>
        </div>
    </div>
</section>

<style>
     .loader{
        width: 100vw;
        height: 100vh;
    }

     .loader-clip{
        position: absolute;
        width: 100vw;
        height: 33vh;
        overflow: clip;
        z-index: 1000;
    }

     .clip-top{
        top: 0;
        clip-path: inset(0 0 0 0);
        background: var(--bg-anim-color);
    }

    .clip-bottom{
        bottom: 0;
        clip-path: inset(0 0 0 0);
        background: var(--bg-anim-color);
    }

    .clip-center{
        overflow: hidden;
        position: relative;
        width: 100vw;
        height: 33vh;
        top: 33vh;
    }

    .marquee{
        position: absolute;
        top: 200%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 200vw;
        font-size: 16vw;
    }

    .marquee-container{
        width: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        font-family: "roboto", sans-serif;
    }
</style>