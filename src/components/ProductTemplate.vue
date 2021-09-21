<template>
    <div class="card-container">
        <div class="product-card">
            <img :src="prod.thumb" :alt="prod.series">
            <span>{{ prod.series }}</span> 
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductTemplate',
    props: ['prod']
}
</script>

<style scoped lang="scss">
    .card-container {
        width: calc((100% / 6) - 30px);
        margin: 15px;

        .product-card {
            width: 100%;
            aspect-ratio: 1/1;
    
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: top;
            }
    
            span {
                display: inline-block;
                color: white;
                text-transform: uppercase;
                font-size: 14px;
                padding: 20px 0;
            }
        }
    }
</style>