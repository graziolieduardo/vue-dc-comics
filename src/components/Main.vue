<template>
    <div>
        <div class="main-top">
            <div class="wrapper">
                <h1> --> Content goes here</h1>
            </div>
        </div>
        <div class="main-bottom">
            <div class="wrapper">
                <ul>
                    <li v-for="(icon, index) in icons" :key="index">
                        <a :href="icon.url">
                            <img :src="require(`../assets/${icon.imgPath + icon.description + icon.extension}`)" alt="">
                            {{ icon.description }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Main',
    data() {
        return {
            icons: [
                {
                    imgPath: 'img/buy-comics-',
                    description: 'digital-comics',
                    extension: '.png',
                    url: '#'
                },
                {
                    imgPath: 'img/buy-comics-',
                    description: 'merchandise',
                    extension: '.png',
                    url: '#'
                },
                {
                    imgPath: 'img/buy-comics-',
                    description: 'shop-locator',
                    extension: '.png',
                    url: '#'
                },
                {
                    imgPath: 'img/buy-comics-',
                    description: 'subscriptions',
                    extension: '.png',
                    url: '#'
                },
                {
                    imgPath: 'img/buy-dc-',
                    description: 'power-visa',
                    extension: '.svg',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/style/var-colors';

    .main-top {
        margin: 0 auto;
        background-color: $black;

        .wrapper {
            width: 70%;
            margin: 0 auto;

            h1 {
                display: flex;
                align-items: center;
                width: 100%;
                height: 150px;
                color: #fff;
            }
        }

    }

    .main-bottom {
        width: 100%;
        height: 150px;
        background-color: $primary-blue;

        .wrapper {
            width: 70%;
            margin: 0 auto;
            height: 100%;

            ul {
                display: flex;
                justify-content: space-between;
                height: 100%;
                padding: 20px;

                li {
                    height: 100%;

                    a {
                        display: flex;
                        align-items: center;
                        height: 100%;
                        text-transform: uppercase;
                        color: #fff;
                        font-size: 14px;
                        
                        img {
                            width: 40px;
                            margin-right: 10px;
                        }
                    }
                }
            }
        }
    }
</style>