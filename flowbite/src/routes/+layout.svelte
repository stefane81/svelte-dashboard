<script>
	import Topbar from '$lib/components/layout/Topbar.svelte';
	import Sidebar from '$lib/components/layout/Sidebar.svelte';
	import '../app.postcss';
</script>

<Topbar />
<Sidebar />
<slot />
