<script>
    let {link, name, frameworks, year} = $props();
</script>

<div class="link w-full flex justify-between items-center">
    <div class="content flex items-center gap-2">
        <a href={link} class="text-(--info) ">{name}</a> :
        <p class=" flex gap-1">
            {#each frameworks as item, i}
                <span>
                    {item} {#if i < frameworks.length -1}, {/if}
                </span>
            {/each}
        </p>
    </div>
    <span>[ {year} ]</span>
</div>

<style>
    a {transition: all .3s ease;}
    a:hover {color: var(--info-hover)}
</style>