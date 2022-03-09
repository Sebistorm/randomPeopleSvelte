<script>
    export let header;
    const capitalHeader = header.charAt(0).toUpperCase() + header.slice(1)
</script>

<div class="tableHeader">{capitalHeader}</div>

<style>
    .tableHeader {
        width: 100%;
        padding: 1rem 2rem;
        border-left: 1px solid white;
        border-right: 1px solid white;
        font-size: 1.5rem;
    }

    .tableHeader:first-child {
        border-left: 0px solid white;
    }

    .tableHeader:last-child {
        border-right: 0px solid white;
    }
</style>
