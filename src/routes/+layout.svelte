<script lang="ts">
    import { Header, Footer } from '$lib/components';
</script>

<Header />

<main>
    <slot />
    <div style="text-align:center; color:white;">
        <h1>Coming soon...</h1>
    </div>
</main>

<Footer />
