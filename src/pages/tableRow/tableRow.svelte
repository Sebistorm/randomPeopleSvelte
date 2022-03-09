<script>
    export let tableRowData; 
    export let size;
</script>

<div style="width: {size}%;" class="tableRow">{tableRowData}</div>

<style>
    .tableRow {
        padding: 1rem 2rem;
        font-size: 1.2rem;
        word-break: break-word;
    }
</style>
