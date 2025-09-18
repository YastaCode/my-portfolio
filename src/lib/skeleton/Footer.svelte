<script>
  import BtnIcon from "$lib/component/BtnIcon.svelte";  
  import { socialIcons } from '$lib/js/socialIcons'
</script>

<footer>
    <div class="flex justify-between items-center mt-4">
        <p>
            &copy; Tous les droits réservés | 
            <a href="/" class="capitalize text-(--info)">yasta code</a>
            2025
        </p>
        <div class="social-icons flex gap-1">
            {#each socialIcons as icon}
                <BtnIcon {...icon} />
            {/each}
        </div>
    </div>
</footer>