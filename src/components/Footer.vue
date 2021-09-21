<template>
    <div>
        <div class="footer-top">
            <div class="wrapper">
                <div class="left">
                    <div class="col">
                        <ul>
                            <h3>dc comics</h3>
                            <li v-for="(item, index) in fComics" :key="index">
                                {{ item.text }}
                            </li>
                        </ul>

                        <ul>
                            <h3>shop</h3>
                            <li v-for="(item, index) in fShop" :key="index">
                                {{ item.text }}
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <h3>dc</h3>
                            <li v-for="(item, index) in fDC" :key="index">
                                {{ item.text }}
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <ul>
                            <h3>sites</h3>
                            <li v-for="(item, index) in fSites" :key="index"> 
                                {{ item.text }}
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="right">
                    <img src="@/assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="wrapper">
                <button>
                    sign-up now!
                </button>

                <div class="social-icons">
                    <span>follow us</span>
                    <ul>
                        <li v-for="(item, index) in socialItems" :key="index">
                            <img :src="require(`@/assets/${item.icon}`)" alt="">
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { footDCComics, footShop, footDC, footSites } from '@/assets/data/links-list.js' 
import socialItems from '@/assets/data/social.js'

export default {
    name: 'Footer',
    data() {
        return {
            fComics: footDCComics,
            fShop: footShop,
            fDC: footDC,
            fSites: footSites,
            socialItems: socialItems
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/style/var-colors';

.footer-top {
    position: relative;
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: #fff;

        .wrapper {
            width: 70%;
            margin: 0 auto;

            &::after {
                content: '';
                display: table;
                clear: both;
            }

            .left {
                float: left;
                width: 50%;
                padding: 40px 0;
        
                .col {
                    float: left;

                    ul {
                        margin: 0 10px;

                        h3 {
                            text-transform: uppercase;
                            margin-bottom: 10px;
                        }
    
                        li {
                            padding: 3px 0;
                            color: #c7c7c7;
                            font-size: 13px;
    
                        }
                    }

                }
            }
        
            .right {
                float: left;
                position: relative;
                width: 50%;
                height: 450px;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                }
            }
        }

}

.footer-bottom {
    height: 120px;
    background-color: #303030;

    .wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 70%;
        height: 100%;
        margin: 0 auto;

        button {
            background-color: #303030;
            border: 2px solid $primary-blue;
            height: max-content;
            padding: 15px 30px;
            color: #fff;
            text-transform: uppercase;
            font-size: 18px;
        }
    
        .social-icons {
            display: flex;
            align-items: center;
            color: $primary-blue;
            text-transform: uppercase;
            font-weight: 600;
            font-size: 18px;
            
            span {
                margin: 10px;
            }

            ul {
                display: flex;
                
                li {
                    margin: 10px;
                }
            }
        }
    }

}
</style>