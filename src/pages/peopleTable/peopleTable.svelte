<script>
    import faker from "@faker-js/faker";
    import TableRow from "../tableRow/tableRow.svelte";
    import TableRowImg from "../tableRow/tableRowImg.svelte";
    import TableHeader from "../tableHead/tableHead.svelte";

    const peopleArray = new Array(faker.datatype.number({min: 1, max: 20})).fill()
    const peopleGeneratedList = peopleArray.map(() => ({
        image: faker.image.avatar(),
        name: faker.name.findName(), 
        email: faker.internet.email(),
        city: faker.address.city(),
        country: faker.address.country()
    }));

    const tableHeaders = Object.keys(peopleGeneratedList[0]);
    const tableRowSize = 100 / tableHeaders.length;
</script>


<div id="tableHead">
    {#each tableHeaders as header }
        <TableHeader header = {header}/>
    {/each}
</div>
<div id="peopleTable">
	{#each peopleGeneratedList as { name, city, email, image, country }}
        <div class="people">
            <TableRowImg img={image} alt={name} size={tableRowSize}/>
            <TableRow tableRowData={name} size={tableRowSize}/>
            <TableRow tableRowData={email} size={tableRowSize}/>
            <TableRow tableRowData={city} size={tableRowSize}/>
            <TableRow tableRowData={country} size={tableRowSize}/>
        </div>
	{/each} 
</div>
<style>
    #peopleTable {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    #tableHead {
        display: flex;
        width: 100%;
        justify-content: space-between;
        background-color: #1B2A38;
        color: white;
    }

    .people {
        width: 100%;
        display: flex;
        background-color: #edf0f5;
    }

    .people:nth-child(2n) {
        background-color: #1B2A38;
        color: white;
    }
</style>

