<script>
    import { contactIcons } from '$lib/js/socialIcons';
    import BtnIcon from "../component/BtnIcon.svelte";

    let {userImg, alt, firstName, lastName, diploma, presenting} = $props();
</script>

<header class="flex flex-col gap-4">
    <div class="info-user flex justify-between items-center gap-4">
        <img src={userImg} alt={alt} class="w-24 rounded-sm border-2 border-(--info)">
        <div class="info">
            <h1 class="capitalize text-5xl">{firstName} <strong>{lastName}</strong></h1>
            <h4 class="uppercase text-right">{diploma}</h4>
            <div class="contact-icons text-right">
                {#each contactIcons as icon}
                    <BtnIcon {...icon} />
                {/each}
            </div>
        </div>
    </div>
    <div class="presenting">
        <h2 class="capitalize text-3xl">profil</h2>
        <p class="text-justify">{@html presenting}</p>
    </div>
</header>