<script>
    import BtnIcon from "$lib/component/BtnIcon.svelte";
    import { home } from '$lib/js/socialIcons'
    const page = {
        link: 'accueil',
        name: 'yasta web'
    }
</script>

<nav class="flex items-end justify-between">
    <div>
        <BtnIcon {...home}/>
        <span class="capitalize">{page.link}</span>
    </div>
    <span class="uppercase font-bold text-(--secondary-bg)">{page.name}</span>
</nav>