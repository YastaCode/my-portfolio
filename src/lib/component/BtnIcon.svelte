<script>
    let {link, arial, icon, target} = $props();
</script>

<a href={link} aria-label={arial} target={target} class="w-6 h-6 text-(--info) hover:text-(--info-hover)">
    <i class="{icon} text-2xl"></i>
</a>

<style>
    a {transition: all .3s ease;}
    a:hover {transform: translateY(-2px);}
</style>