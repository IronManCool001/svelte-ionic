<script>
	import Nav from "../components/Nav.svelte";
	export let segment;
</script>
<svelte:options tag={null}/>
<style>
</style>

<ion-app>
	<ion-page>
	<Nav currentPage={segment}/>
	<slot></slot>
	</ion-page>
</ion-app>
