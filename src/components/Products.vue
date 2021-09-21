<template>
    <div>
        <div class="main-top">
            <div class="wrapper">
                <div class="section-title">
                    <h1>Current Series</h1>
                </div>
                <ProductTemplate
                v-for="(product, index) in products"
                :key="index"
                :prod="product"
                />
                <button>Load More</button>

            </div>
        </div>
    </div>
</template>

<script>
import ProductTemplate from '@/components/ProductTemplate.vue'
import ProductsJson from '@/assets/data/dc-comics.json'

export default {
    name: 'Products',
    components: {
        ProductTemplate,
    },
    data() {
        return {
            products: ProductsJson
        }
    }

}
</script>

<style scoped lang='scss'>
@import '@/assets/style/var-colors';

    .main-top {
        margin: 0 auto;
        background-color: $black;

        .wrapper {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            position: relative;
            width: 70%;
            margin: 0 auto;
            padding: 50px 0px 20px;

            h1 {
                position: absolute;
                left: 0;
                top: 0;
                transform: translateY(-50%);
                padding: 10px 30px;
                background-color: $primary-blue;
                color: white;
            }

            button {
                padding: 10px 50px;
                border-radius: 0px;
                border: none;
                background-color: $primary-blue;
                color: white;
                text-transform: uppercase;
                font-weight: bold;
            }
        }

    }
</style>