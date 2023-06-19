<script lang="ts">
    import { Navigation, Logo } from '$lib/components';
</script>

<header>
    <Logo />
    <Navigation />
</header>

<style lang="scss">
    header {
        display: grid;
        grid-template-columns: auto 1fr;
        align-items: center;
        padding-block: 0.8rem;
        padding-inline: 1.5rem;
    }
</style>
