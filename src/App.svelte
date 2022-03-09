<script>
	import PeopleTable  from "./pages/peopleTable/peopleTable.svelte"; 
</script>

<h1>Table of random people</h1>

<PeopleTable/>


<style>
	:global(body) {
		max-width: 1024px;
		margin: 0 auto;
	}

	:global(*) {
		box-sizing: border-box;
	}
</style>
