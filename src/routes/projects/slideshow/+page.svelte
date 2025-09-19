<script>
    import BtnIcon from "$lib/component/BtnIcon.svelte";
    import { home } from "$lib/js/socialIcons";
    import { slideGalapagos } from "$lib/js/slides";
    import SlideshowCarousel from "$lib/slideshows/SlideshowCarousel.svelte";
    
    const page = {
        link: 'slideshows',
        name: 'yasta web'
    }
</script>

<nav class="flex items-end justify-between pb-2">
    <div class="flex items-center">
        <BtnIcon {...home}/>
        <i class="bx bx-chevron-right text-xl"></i>
        <span class="capitalize">{page.link}</span>
    </div>
    <span class="uppercase font-bold text-(--secondary-bg)">{page.name}</span>
</nav>

<main>
    <h2 class="text-4xl">Mes Slideshow Ultra Moderne</h2>
    <section>
        <h3 class="text-2xl text-right">Slideshow Carousel</h3>
        <p>Slideshow Carousel avec SvelteKit, Tailwind CSS et JavaScript, personnalisé que inclue : </p>
        <ul>
                <li>Import du tableau contenant les images et les captions.</li>
                <li>Fonctions <code>(showSlide, plusSlide, currentSlide)</code> pour naviguer entre les slides.</li>
                <li><code>#each</code> pour itérer sur les slides.</li>
                <li>Utilisation de <code>class:hidden</code> pour cacher les slides non actifs.</li>
                <li>Utilisation de <code>onclick</code> pour les boutons de navigations.</li>
                <li>Animation de <code>fade</code> avec une cléframe.</li>
            </ul>
        <SlideshowCarousel {slideGalapagos} />
    </section>
</main>

<style>
    ul {
        list-style: disc;
        margin-left: 2rem;
        margin-bottom: 1rem;
    }
</style>