<script>
import Router from 'svelte-spa-router'
import routes from './routes';

import Menu from './Componentes/Menu.svelte';
import Footer from './Componentes/Footer.svelte';
import Botones from './Componentes/Botones.svelte';
</script>

<main>
<Menu />
<!-- <Botones /> -->
<Router {routes} />
<Footer />
</main>

<style>

</style>