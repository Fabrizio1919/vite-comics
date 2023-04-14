<script>
export default {
    name: 'ItemsComicx',
    props: {
        thumb: String,
        price: String,
        series: String,
    }
}

</script>


<template>
<div class="col">
    <div class="itemsComicx">
        <img class="itemsImg" :src="thumb" alt="series + 'Image'">
        <h3>{{ series }}</h3>
        <div class="price">
            <p>{{ price }}</p>
        </div>
    </div>
</div>
        
    
</template>

<style>


</style>