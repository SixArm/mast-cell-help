<script>
import "../app.postcss";
import Header from "$lib/Header.svelte";
import Footer from "$lib/Footer.svelte";
export const prerender = true;
export const trailingSlash = 'always';
</script>
<Header />
<slot />
<Footer />
