<script>
    export let img;
    export let alt; 
    export let size;
</script>

<img style="width: {size}%;" class="tableRow tableRowImg" src="{img}" alt="{alt}">

<style>
    .tableRowImg {
        height: 100px;
        object-fit: contain;
    }
</style>