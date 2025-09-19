<script>
    import { projectList } from '$lib/js/projectsList';
    import Link from '../component/Link.svelte';
</script>

<article class="flex flex-col gap-2">
    <h3 class="text-2xl">List de Projets</h3>
    <ul>
        {#each projectList as item}
            <li class="flex">
                <Link 
                    name={item.name} 
                    frameworks={item.frameworks} 
                    year={item.year} 
                    link={item.link} 
                />
            </li>
        {/each}
    </ul>
</article>