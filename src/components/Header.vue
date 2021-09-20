<template>
    <div>
        <div class="margin-start"></div>
        <header>
            <div class="wrapper">
                <div class="logo-container">
                    <img src="@/assets/img/dc-logo.png" alt="">
                </div>
                <div class="nav-container">
                    <ul>
                        <li v-for="(link, index) in links" :key="index" :class="(link.active) ? 'active' : null">
                            <a :href="link.url">
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </header>
    </div>
</template>

<script>
import Links from '@/assets/js/nav-list'

export default {
    name: 'Header',
    data() {
        return {
            links: Links
        }
    }
}
</script>

<style scoped lang="scss">
@import '@/assets/style/var-colors';
    
    .margin-start {
        height: 30px;
        background-color: $black;
    }

    header {
        width: 100%;
        height: 120px;
        background-color: #fff;

        .wrapper {
            width: 70%;
            height: 100%;
            margin: 0 auto;
        }

        .logo-container,
        .nav-container {
            float: left;
        }

        .logo-container {
            display: flex;
            align-items: center;
            width: 40%;
            height: 100%;

            img {
                width: 80px;
            }
        }

        .nav-container {
            width: 60%;
            height: 100%;
            font-size: 12px;

            ul {
                display: flex;
                align-items: center;
                height: 100%;

                li {
                    display: flex;
                    align-items: center;
                    height: 100%;
                    margin: 0 15px;
                    text-transform: uppercase;

                    &.active {
                        border-bottom: 3px solid $primary-blue;

                        a {
                            color: $primary-blue;
                        }
                    }

                    &:hover {
                        border-bottom: 3px solid $primary-blue;
                    }

                    a {
                        color: $secondary-darkgray;
    
                        &:hover {
                            color: $primary-blue;
                        }
                    }
                }
            }

        }
    }
</style>