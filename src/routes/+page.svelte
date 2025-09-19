<script>
    import BtnIcon from "$lib/component/BtnIcon.svelte";
    import Header from "$lib/skeleton/Header.svelte";   
    import { home } from '$lib/js/socialIcons';
    import { infoUser } from '$lib/js/infoUser';
    import ProjectList from "$lib/skeleton/ProjectList.svelte";
    const page = {
        link: 'accueil',
        name: 'yasta web'
    }
</script>

<nav class="flex items-end justify-between pb-2">
    <div class="flex items-center gap-1">
        <BtnIcon {...home}/>
        <span class="capitalize">{page.link}</span>
    </div>
    <span class="uppercase font-bold text-(--secondary-bg)">{page.name}</span>
</nav>

<main>
    <section><Header {...infoUser} /></section>
    <section><ProjectList /></section>
</main>